---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275513"
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

---
## <a name="6120---november-2018"></a>6.12.0 - novembro de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Atualizar código comum para usar a versão mais recente do ClientRuntime
* Renomear o parâmetro TenantId no cmdlet Connect-AzureRmAccount do locatário e adicionar um alias para TenantId
* Descrição de TenantId atualizada para Connect-AzureRmAccount
* Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário
    - https://github.com/Azure/azure-powershell/issues/6936
* Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário
    - https://github.com/Azure/azure-powershell/issues/7453
* Corrigir o problema com pontos de extremidade DataLake ao usar o MSI
    - https://github.com/Azure/azure-powershell/issues/7462
* Corrigir o problema em que 'Disconnect-AzureRmAccount' seria lançado se não conectado
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* Nome do arquivo DLL de cmdlet renomeado para Microsoft.Azure.Commands.Automation.dll

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Adicionar operação Get-AzureRmCognitiveServicesAccountSkus.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Adicionar cmdlets Add-AzureRmVmssVMDataDisk e Remove-AzureRmVmssVMDataDisk
* Get-AzureRmVMImage mostra AutomaticOSUpgradeProperties
* Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzureRmVMChefExtension corrigidos não estão de acordo com a configuração no formato json.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Atualizar o pacote de DataLake para 1.1.10.
* Adicionar o padrão de Simultaneidade às operações multi-threaded.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Correção do problema #7267 (área de dimensionamento automático)
    - Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).
* Correção do problema #7513 [Insights] Set-AzureRMDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração
    - Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado

#### <a name="azurermnetwork"></a>AzureRM.Network
* Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Adicionados cmdlets de correção de política

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Adicionado suporte para compartilhamentos de arquivos do Azure nos serviços de recuperação.

#### <a name="azurermresources"></a>AzureRM.Resources
* Correção para https://github.com/Azure/azure-powershell/issues/7402
    - Permitir a listagem de recursos usando o parâmetro '-ResourceId' para 'Get-AzureRmResource'

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Correção do certificado de adição para Vmss do Linux.
* Corrigir 'Add-AzureRmServiceFabricClusterCertificate'
    - Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).
    - Exibir exceções corretamente (Azure/service-fabric-issues#1054).
* Corrigir 'Update-AzureRmServiceFabricDurability' para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.

## <a name="6110---october-2018"></a>6.11.0 - Outubro de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Corrigir o problema com Get-AzureRmSubscription no CloudShell
* Atualizar código comum para usar a versão mais recente do ClientRuntime

#### <a name="azurermbackup"></a>AzureRM.Backup
* Cmdlets do Backup do Azure preteridos.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para 'New-AzureRmVm'
* Adicionado o finalizador do argumento ResourceName para todos os cmdlets.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Adicionar suporte às Regras de Rede Virtual
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: obtém ou lista regras de rede virtual do Azure Data Lake Store.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: adiciona uma regra de rede virtual para a conta do Data Lake Store especificada.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: exclui uma regra de rede virtual do Azure Data Lake Store.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Atualize o cmdlet Test-AzureRmNetworkWatcherConnectivity, passe o valor de protocolo para o back-end.
* Adicionado o finalizador do argumento ResourceName para todos os cmdlets.

#### <a name="azurermresources"></a>AzureRM.Resources
* Corrija o problema onde Get-AzureRMRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário. Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.

## <a name="6100---october-2018"></a>6.10.0 – outubro de 2018
#### <a name="azurestorage"></a>Azure.Storage
* Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Suporte para Get-AzureRmCognitiveServicesAccountSkus sem uma conta existente.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Correção de Get-AzureRmVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário
* Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzureRmVmss.
* Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Atualizada a versão do SDK do ADF .NET para 2.3.0.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Adicionada a funcionalidade NetworkProfile. Novos cmdlets adicionados
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Link de associação de serviço adicionado no modelo de sub-rede
* Adicionados os cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap
* Adicionados os cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante. Adição do P5 na pop-up PSArgumentCompleter

#### <a name="azurermresources"></a>AzureRM.Resources
* Adição do parâmetro -Mode ausente a Set-AzureRmPolicyDefinition
* Correção do bug do cmdlet Get-AzureRmProviderOperation para operações com a Origem que contém o Usuário

#### <a name="azurermsql"></a>AzureRM.Sql
* Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure

#### <a name="azurermstorage"></a>AzureRM.Storage
* O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Novo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner
* Novos cmdlets New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows

## <a name="690---september-2018"></a>6.9.0 - setembro de 2018
#### <a name="general"></a>Geral
* O AzureRM.SignalR foi adicionado ao módulo de rollup do AzureRM

#### <a name="azurermprofile"></a>AzureRM.profile
* Pequenas alterações no código comum de armazenamento
* Arquivos de ajuda atualizados para incluir tipos de parâmetro completos.
* Alterado: ServicePrincipal como não obrigatório no conjunto de parâmetros ServicePrincipalCertificateWithSubscriptionId 

#### <a name="azurestorage"></a>Azure.Storage
* Suporte à criação do Contexto de Armazenamento com OAuth. 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Standard_Microsoft adicionado à SKU de preços da CDN. 

#### <a name="azurermcompute"></a>AzureRM.Compute
* Mover dependências em Keyvault e Armazenamento para as dependências em comum
* Adicionar suporte aos cmdlets do AEM para mais tamanhos de máquina virtual
* Adicionar o parâmetro PublicIPPrefix a New-AzureRmVmssIpConfig
* Adicionar parâmetro ResourceId ao cmdlet Invoke-AzureRmVMRunCommand
* Adicionar cmdlet Invoke-AzureRmVmssVMRunCommand

#### <a name="azurermdns"></a>AzureRM.Dns
* Suporte adicionado ao registro de alias durante criação de registros DNS

#### <a name="azurerminsights"></a>AzureRM.Insights
* Problemas 6833 e 7102 corrigidos (área Configurações de Diagnóstico)
    - Problemas com o nome padrão, ou seja, “service”, durante a criação e a listagem/obtenção das configurações de diagnóstico
    - Problemas na criação das configurações de diagnóstico com categorias
* Mensagem de reprovação adicionada para parâmetros do intervalo de agregação de métrica
    - Os parâmetros do intervalo de agregação ainda são aceitos (é uma alteração contínua), mas eles são ignorados no back-end, já que só PT1M é válido

#### <a name="azurermnetwork"></a>AzureRM.Network
* Alterações nos cmdlets LoadBalancer
  - LoadBalancerInboundNatPoolConfig: parâmetros IdleTimeoutInMinutes, EnableFloatingIp e EnableTcpReset adicionados
  - LoadBalancerInboundNatRuleConfig: parâmetro EnableTcpReset adicionado
  - LoadBalancerRuleConfig: parâmetro EnableTcpReset adicionado
  - LoadBalancerProbeConfig: suporte adicionado para o valor "Https" do parâmetro Protocol
* Adicionados novos comandos para o novo sub-recurso OutboundRule do LoadBalancer
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* Nova propriedade HostedWorkloads adicionada para PSNetworkInterface
* Novos cmdlets adicionados para o recurso: Firewall do Azure via ARM
  - Get-AzureRmFirewall adicionado
  - Set-AzureRmFirewall adicionado
  - New-AzureRmFirewall adicionado
  - Remove-AzureRmFirewall adicionado
  - New-AzureRmFirewallApplicationRuleCollection adicionado
  - New-AzureRmFirewallApplicationRule adicionado
  - New-AzureRmFirewallNatRuleCollection adicionado
  - New-AzureRmFirewallNatRule adicionado
  - New-AzureRmFirewallNetworkRuleCollection adicionado
  - New-AzureRmFirewallNetworkRule adicionado
* Suporte adicionado para o certificado de Raiz Confiável e a configuração de Dimensionamento automático no Gateway de Aplicativo
  - Novos Cmdlets adicionados:
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - Cmdlets atualizados com o parâmetro opcional -TrustedRootCertificate
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - Cmdlets atualizados com o parâmetro opcional -AutoscaleConfiguration
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* Adicionar cmdlet para o Ponto de Extremidade da interface Get-AzureInterfaceEndpoint
* Suporte adicionado para vários prefixos de endereço em uma sub-rede. Cmdlets atualizados:
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Adicionando cmdlets para delegação da sub-rede.
  - New-AzureRmDelegation: cria uma nova delegação que pode ser adicionada a uma sub-rede
  - Remove-AzureRmDelegation: usa uma sub-rede e remove o nome de delegação fornecido dela
  - Add-AzureRmDelegation: usa uma sub-rede e adiciona o nome do serviço fornecido como uma delegação para essa sub-rede
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Suporte ao disco gerenciado

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Dependência do Insights atualizada.

#### <a name="azurermresources"></a>AzureRM.Resources
* Atualizar New-AzureRmResourceGroupDeployment com o novo parâmetro RollbackAction
    - Adicionar suporte a OnErrorDeployment com o novo parâmetro
* Suporte à identidade gerenciada nas atribuições de política.
* Os parâmetros com valores padrão não são mais necessários ao atribuir uma política com “New-AzureRmPolicyAssignment”
* Adicionar novo cmdlet Get-AzureRmPolicyAlias para recuperar os aliases de política

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Problema corrigido 7161

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* Atualizar nomes de SKU para Free_F1 e Standard_S1
* Adicionar campo de versão ao objeto PSSignalRResource e a cadeia de conexão ao objeto PSSignalRKeys.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Suporte à Política de Imutabilidade no AzureRm.Storage 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Dois novos cmdlets adicionados: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp
* O argumento New-AzureRmAppServicePlan-HyperV é adicionado para criar um plano do serviço de aplicativo com o contêiner do Windows
* New-AzureRmWebApp/New-AzureRmWebAppSlot/ Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Novos parâmetros (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) adicionados para criar e gerenciar o aplicativo de contêiner do Windows

## <a name="681---august-2018"></a>6.8.1 - Agosto de 2018
#### <a name="general"></a>Geral
* Corrigido o problema com os grupos de recursos padrão não sendo definidos.
* Assemblies de tempo de execução comum atualizados

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Corrigido o problema com os grupos de recursos padrão não sendo definidos.
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6603
    - Os cmdlets Importar-AzureRmApiManagementApi e *-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6879
    - O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente. Corrigida pela atualização para o nuget 4.0.4-nuget de prévia
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6853
    - Corrigido o filtro Odata para pesquisar por nome no produto
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6814
    - Corrigido o filtro Odata para pesquisar por nome na API
* Adicionado suporte para o agente de AzureMonitor


#### <a name="azurermcompute"></a>AzureRM.Compute
* Corrigido o problema onde o destino está ausente na saída de erro.
* Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado
* Corrigido o problema com os grupos de recursos padrão não sendo definidos.
* Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China

#### <a name="azurermnetwork"></a>AzureRM.Network
* Alterada a representação de saída de cmdlet para exibição de tabela

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa


#### <a name="azurermresources"></a>AzureRM.Resources
* Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Problemas corrigidos
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Suporte adicionado para o método de roteamento de vários valores
    - Novo parâmetro “MaxReturn” para o roteamento de vários valores
* Suporte adicionado para o método de roteamento de sub-rede
    - Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade
* Suporte adicionado para cabeçalhos personalizados nos perfis
* Suporte adicionado para intervalos de código de status esperados em perfis
* Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade

## <a name="680---august-2018"></a>6.8.0 - Agosto de 2018
#### <a name="general"></a>Geral
* Corrigido o problema com os grupos de recursos padrão não sendo definidos.

#### <a name="azurermprofile"></a>AzureRM.profile
* Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount

#### <a name="azurermcompute"></a>AzureRM.Compute
* Corrigido o problema onde o destino está ausente na saída de erro.
* Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado
* Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices

#### <a name="azurermnetwork"></a>AzureRM.Network
* Alterada a representação dos modelos padrão para exibição de tabela

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa

#### <a name="azurermresources"></a>AzureRM.Resources
* Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Correção de problemas
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Suporte para o método de roteamento de vários valores
    - Novo parâmetro “MaxReturn” para o roteamento de vários valores
* Suporte para o método de roteamento de sub-rede
    - Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade
* Suporte para cabeçalhos personalizados nos perfis
* Suporte para intervalos de código de status esperados em perfis
* Suporte para cabeçalhos personalizados nos pontos de extremidade

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.

## <a name="670---august-2018"></a>6.7.0 - agosto de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Atualização para a versão mais recente do Azure ClientRuntime.
* Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos
    - https://github.com/Azure/azure-powershell/issues/6489
* Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398
* Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Atualização para a versão mais recente do Azure ClientRuntime.
* Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig
* Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.
* Corrigir a descrição do parâmetro em Save-AzureRmVMImage
* Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Corrigir depuração quando DebugPreference for definido na linha de comando do powershell
* Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl
* Atualização para a versão mais recente do Azure ClientRuntime.
* Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermdns"></a>AzureRM.Dns
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermmedia"></a>AzureRM.Media
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Exemplo adicionado para Set-AzureRmLocalNetworkGateway
* Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection
* Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway
* Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey
* Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey
* Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection
* Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente
* Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem. O comando retorna a lista de itens de backup protegidos pela id de política dada.
* Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.
* Atualização para a versão mais recente do Azure ClientRuntime.
* Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem. O grupo de recursos para o qual os discos gerenciados são restaurados. Aplicável ao backup da VM com discos gerenciados.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermresources"></a>AzureRM.Resources
* Suporte à implantação de modelos no escopo da assinatura. Adicione novos Cmdlets:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource
    - https://github.com/Azure/azure-powershell/issues/5705
* Corrigir exemplo em New-AzureRmResourceGroupDeployment
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermsql"></a>AzureRM.Sql
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermtags"></a>AzureRM.Tags
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Atualização para a versão mais recente do Azure ClientRuntime.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Atualização para a versão mais recente do Azure ClientRuntime.

## <a name="660---july-2018"></a>6.6.0 – Julho de 2018
#### <a name="general"></a>Geral
* Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.

#### <a name="azurermprofile"></a>AzureRM.profile
* Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.
* Tipos de ps1xml adicionados a Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile
* Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6370
    - Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6515
    - Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6560
    - Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId

#### <a name="azurermcompute"></a>AzureRM.Compute
* Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.
* Corrigir o cmdlet Invoke-AzureRmVMRunCommand
* Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.  (O parâmetro ResouceGroupName agora é opcional.)
* Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.
* Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.
* Atualizar exemplo de New-AzureRmDisk
* Adicionar exemplo de 'New-AzureRmVM'
* Atualizar descrição de Set-AzureRmVMOSDisk
* Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Atualizado a versão do SDK do .NET do ADF para 1.1.0.
* Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.
     - Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Tubulação atualizada para InputObject e ResourceId em Remover cmdlets

#### <a name="azurerminsights"></a>AzureRM.Insights
* Formatação corrigida do OutputType nos arquivos de ajuda
* Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.

#### <a name="azurermresources"></a>AzureRM.Resources
* Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'
    - https://github.com/Azure/azure-powershell/issues/6765
* Corrigir o cenário de tubulação com 'Set-AzureRmResource'

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Tubulação atualizada para InputObject e ResourceId em Remover cmdlets
* alguns problemas corrigidos
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule
* Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog

#### <a name="azurermstorage"></a>AzureRM.Storage
* Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets
* Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Remover instrução incorreta de ajuda de cmdlet de marca
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - julho de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'

#### <a name="azurestorage"></a>Azure.Storage
* Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Adicione a propriedade necessária ResourceGroupName ao AS.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'

#### <a name="azurermcompute"></a>AzureRM.Compute
* Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet
* Adicionar exemplo do 'Add-AzureRmVmssExtension'
* Adicionar exemplos do 'Remove-AzureRmVmssExtension'
* Atualizar ajuda do 'Set-AzureRmVMAccessExtension'
* Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp

#### <a name="azurermnetwork"></a>AzureRM.Network
* Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering
* Atualizados os cmdlets abaixo para o Gateway de Aplicativo
    - New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas
    - New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2
    - Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2
* Cmdlets de RouteTable regenerados com a versão mais recente do gerador

#### <a name="azurermrelay"></a>AzureRM.Relay
* Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo

#### <a name="azurermresources"></a>AzureRM.Resources
* Atualize os cmdlets Roleassignment e roledefinition:
    - Remova chamadas extras roledefinition feitas como parte da paginação.
* Corrigir cmdlet Get-AzureRmRoleAssignment
    - Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups
* Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Adicionado o parâmetro top e skip aos cmdlets de lista
* Adicionados os cmdlets de migração de NameSpace Standard a Premium:
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Exemplo de atualização para 'New-AzureRmServiceFabricCluster'

#### <a name="azurermsql"></a>AzureRM.Sql
* Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.
* Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados
* `Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida

## <a name="640---july-2018"></a>6.4.0 - julho de 2018
#### <a name="general"></a>Geral
* Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos

#### <a name="azurermprofile"></a>AzureRM.profile
* Atributo Ps1Xml adicionado aos tipos de saída básicos

#### <a name="azurermcompute"></a>AzureRM.Compute
* Recurso de Marca do IP para VMSS
    - O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado
    - O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig
* Recurso de Reversão Automática do SO para VMSS
    - Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss
* Recurso do Histórico de Atualizações do SO para Vmss
    - O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Adicione suporte para as ACLs de Catálogo com os comandos a seguir:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties
* Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas
* Corrigir local de teste dos cmdlets DataLake

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup
* Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub. Conjunto de Parâmetros Padrão fornecido.
* Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag

#### <a name="azurermnetwork"></a>AzureRM.Network
* Expor novas Skus para VirtualNetworkGateways com Redundância de Zona
* Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM
    - Get-AzureRmExpressRouteCrossConnection adicionado
    - Set-AzureRmExpressRouteCrossConnection adicionado
    - Add-AzureRmExpressRouteCrossConnectionPeering adicionado
    - Get-AzureRmExpressRouteCrossConnectionPeering adicionado
    - Remove-AzureRmExpressRouteCrossConnectionPeering adicionado
    - Get-AzureRMExpressRouteCrossConnectionArpTable adicionado
    - Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado. Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura. Se houver tal cofre, o cmdlet produzirá detalhes dele.

#### <a name="azurermresources"></a>AzureRM.Resources
* Atualize os cmdlets Get-AzureRmPolicyAssignment:
    - Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento
    - Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento
    - Adicionar argumentos -Effective e -All para controlar  parâmetro
* Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition
    - Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento
    - Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura
* Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition
    - Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento
    - Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura
* Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”
* Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”
    - https://github.com/Azure/azure-powershell/issues/6505
* Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.

#### <a name="azurermsql"></a>AzureRM.Sql
* Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint
* Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets

## <a name="630---june-2018"></a>6.3.0 - junho de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave
* Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior

#### <a name="azurestorage"></a>Azure.Storage
* Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.

#### <a name="azurermcompute"></a>AzureRM.Compute
* “Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados 
* Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzureRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Versão pública dos cmdlets de Informações sobre a Política
    - Usar versão da API 2018-04-04
    - Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup. Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig

#### <a name="azurermwebsites"></a>AzureRM.Websites
* "Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity
* "New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional

## <a name="621---june-2018"></a>6.2.1 - junho de 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro

## <a name="620---june-2018"></a>6.2.0 - Junho de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo

#### <a name="azurermcompute"></a>AzureRM.Compute
* Recurso de atualização de VM VMSS
    - Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados
    - Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:
    - A operação para Configurar o repositório de fábrica foi adicionada
    - O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret
    - Vários tipos de modelo atualizados de SecretBase para Object
    - Foram adicionados gatilho de eventos de blob

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Atualizar documentação com a saída de exemplo

### <a name="azurermnetwork"></a>AzureRM.Network
* Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede

#### <a name="azurermresources"></a>AzureRM.Resources
* Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação

### <a name="azurermsql"></a>AzureRM.Sql
* Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.

## <a name="610---may-2018"></a>6.1.0 - maio de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Habilite as operações de associação/desassociação do Gateway no sistema autônomo.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions
* Suporte adicionado para Back-end do ServiceFabric
* Suporte adicionado para Agente do Application Insights
* Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api
* Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA
* Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy
* Suporte adicionado para a identidade MSI
* Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Versão do novo cmdlet Get-AzureBatchPoolNodeCounts
* Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties
* Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry 
* Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview
* Cmdlet adicionado para criar a configuração de protocolo
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet adicionado para recuperar uma conexão de circuito
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups
* Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política. Envie a solicitação com a nova política de retenção flexível”.
* Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.
* Os cmdlets atualizados, incluindo: 
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.
