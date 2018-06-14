---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854606"
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

## <a name="version-220"></a>Versão 2.2.0
* Computação
  - Adicionar suporte para consultar o status da criptografia a partir da extensão AzureDiskEncryptionForLinux
* DataFactory
  - Novo cmdlet adicionado para listar as janelas de atividade
    + Get-AzureRmDataFactoryActivityWindow
* DataLake
  - Parâmetro alterado `Host` para `DatabaseHost` e alias adicionado a `Host`
    + New-AzureRmDataLakeAnalyticsCatalogSecret
    + Set-AzureRmDataLakeAnalyticsCatalogSecret
  - Adicionar suporte para a ACL e a remoção da ACL padrão
  - Adicionar suporte para obter e definir permissões sem nome em arquivos e pastas
* KeyVault
  - Adicionar suporte para certificados
    + Add-AzureKeyVaultCertificate
    + Add-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificate
    + Get-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificateIssuer
    + Get-AzureKeyVaultCertificateOperation
    + Get-AzureKeyVaultCertificatePolicy
    + Import-AzureKeyVaultCertificate
    + New-AzureKeyVaultCertificateAdministratorDetails
    + New-AzureKeyVaultCertificateOrganizationDetails
    + New-AzureKeyVaultCertificatePolicy
    + Remove-AzureKeyVaultCertificate
    + Remove-AzureKeyVaultCertificateContact
    + Remove-AzureKeyVaultCertificateIssuer
    + Remove-AzureKeyVaultCertificateOperation
    + Set-AzureKeyVaultCertificateAttribute
    + Set-AzureKeyVaultCertificateIssuer
    + Set-AzureKeyVaultCertificatePolicy
    + Stop-AzureKeyVaultCertificateOperation
* Rede

  - Novo parâmetro de opção adicionado ao adaptador de rede para habilitar/desabilitar o +New-AzureRmNetworkInterface -EnableAcceleratedNetworking de redes aceleradas
  - Habilitar cmdlets do PowerShell de recurso do gateway de Ativo-Ativo
    + Add-AzureRmVirtualNetworkGatewayIpConfig
    + Remove-AzureRmVirtualNetworkGatewayIpConfig
  - Novo cmdlet adicionado
    + Test-AzureRmPrivateIpAddressAvailability
* Recursos
  - Suporte a zonas nos cmdlets do provedor e de recursos
    + Get-AzureRmProvider
    + New-AzureRmResource
    + Set-AzureRmResource
* Sql
  - Novos cmdlets adicionados para o gerenciamento das políticas de detecção de ameaças do SQL Azure no nível do servidor
    + Get-AzureRmSqlServerThreatDetectionPolicy
    + Remove-AzureRmSqlServerThreatDetectionPolicy
    + Set-AzureRmSqlServerThreatDetectionPolicy
  - Novos cmdlets adicionados para oferecer suporte para habilitar/desabilitar a GeoBackupPolicy do Sql Azure DataWarehouses
    + Get-AzureRmSqlDatabaseGeoBackupPolicy
    + Set-AzureRmSqlDatabaseGeoBackupPolicy
  - Novos cmdlets adicionados para os Assistentes do Sql Azure e APIs de Ações Recomendadas
    + Get-AzureRmSqlDatabaseAdvisor
    + Get-AzureRmSqlElasticPoolAdvisor
    + Get-AzureRmSqlServerAdvisor
    + Get-AzureRmSqlDatabaseRecommendedActions
    + Get-AzureRmSqlElasticPoolRecommendedActions
    + Get-AzureRmSqlServerRecommendedActions
    + Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus
    + Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus
    + Set-AzureRmSqlServerAdvisorAutoExecuteStatus
    + Set-AzureRmSqlDatabaseRecommendedActionState
    + Set-AzureRmSqlElasticPoolRecommendedActionState
    + Set-AzureRmSqlServerRecommendedActionState
