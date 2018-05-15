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
ms.date: 05/18/2017
ms.openlocfilehash: 04f89e8d47d0825d46cb1b8817efbcc0cafa0acd
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

## <a name="version-380"></a>Versão 3.8.0
* Computação
  - Corrigir um bug nos cmdlets Get-* para permitir a recuperação de várias páginas de dados (mais de 120 itens)
* DataLakeAnalytics
  - Corrija a ajuda de alguns comandos para ter a devida explicação e exemplos.
* DataLakeStore
  - Adicione suporte do início e final ao cmdlet `Get-AzureRMDataLakeStoreItemContent`. Isso permite retornar as linhas, a serem exibidas, delimitadas pelo caractere de nova linha com o primeiro ou último N.
* HDInsight
  - Suporte adicionado para o tipo de cluster RServer
    + O tamanho da VM Edgenode pode ser especificado para o cluster RServer em New-AzureRmHDInsightCluster ou New-AzureRmHDInsightClusterConfig
    + Agora, RServer é uma opção de configuração em Add-AzureRmHDInsightConfigValues. Permite que o sinalizador RStudio seja definido para indicar que a instalação do RStudio deve ser feita.
* LogicApp
  - Os cmdlets Set-AzureRmIntegrationAccountSchema e Set-AzureRmIntegrationAccountMap são corrigidos para o problema do contentlink (o conteúdo e o contentlink foram definidos, resultando em uma falha de atualização).
* Rede
  - Suporte adicionado dos novos recursos de firewall do aplicativo Web para os Gateways de Aplicativo
    + New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig adicionado
    + Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets) adicionado
    + New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration atualizado: parâmetros adicionados -RuleSetType -RuleSetVersion e -DisabledRuleGroups
    + Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration atualizado: parâmetros atualizados -RuleSetType -RuleSetVersion e -DisabledRuleGroups
  - Suporte adicionado das políticas IPSec para as Conexões de Gateway da Rede Virtual
  - New-AzureRmIpsecPolicy adicionado
  - New-AzureRmVirtualNetworkGatewayConnection atualizado: parâmetros adicionados -IpsecPolicies e -UsePolicyBasedTrafficSelectors
* Perfil
  - *Obsoleto*: Save-AzureRmProfile é renomeado como Save-AzureRmContext, há um alias para o antigo nome do cmdlet, o alias será removido na próxima versão.
  - *Obsoleto*: Select-AzureRmProfile é renomeado como Import-AzureRmContext, há um alias para o antigo nome do cmdlet, o alias será removido na próxima versão.
  - Os tipos de saída PSAzureContext e PSAzureProfile dos cmdlets de perfil serão alterados na próxima versão.
  - O cmdlet Save-AzureRmContext não terá nenhum OutputType na próxima versão.
  - Corrija o bug no código comum do cmdlet para usar um algoritmo compatível com o FIPS dos hashes de dados: https://github.com/Azure/azure-powershell/issues/3651
* Sql
  - Correções de bugs nos Cmdlets do Grupo de Failover do Azure
  - Corrigir para sondagem da operação
  - Corrigir o valor GracePeriodWithDataLossHour ao definir a FailoverPolicy para Manual
* TrafficManager
  - Suporte para o método de roteamento de tráfego Geográfico
    + Novo valor 'Geográfico' para o parâmetro TrafficRoutingMethod de New-AzureRmTrafficManagerProfile
    + Novo parâmetro ‘GeoMapping’ para New-AzureRmTrafficManagerEndpoint e Add-AzureRmTrafficManagerEndpointConfig
    + Corrigir o direcionamento de Get-AzureRmTrafficManagerProfile quando ele retorna uma coleção de perfis
* ServiceManagement
  - Restart-AzureVM: parâmetro InitiateMaintenance adicionado para executar a manutenção durante a reinicialização da VM.
  - Get-AzureVM: campo do Status da Manutenção adicionado.
  - Novos cmdlets adicionados para oferecer suporte à atualização do cofre dos Serviços de Recuperação
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
