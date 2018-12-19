---
title: Visão geral do Azure Stack Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Admin PowerShell com instruções de instalação e configuração.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216612"
---
# <a name="azure-stack-module-150"></a>Módulo do Azure Stack 1.5.0

## <a name="requirements"></a>Requisitos:
A versão mínima do Azure Stack com suporte é 1808.

Observação: Se você estiver usando uma versão anterior, instale a versão 1.4.0

## <a name="known-issues"></a>Problemas conhecidos:

- O New-AzsOffer não permite criar uma oferta com o estado público. O cmdlet Set-AzsOffer precisa ser chamado depois para alterar o estado.
- Um Pool de IPs não pode ser removido sem uma reimplantação

## <a name="install"></a>Instalar
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a>Notas de versão
* Todos os módulos do Azure Stack Admin foram atualizados para dependência maior que ou igual a no módulo AzureRM.Profile
* Suporte para lidar com nomes de recurso aninhado em todos os módulos
* Correção de bug em todos os módulos em que ErrorActionPreference está sendo substituído por Stop
* Módulo Azs.Compute.Admin
    * Novas propriedades de cota adicionadas para o suporte de disco gerenciado
    * Adição de cmdlets relacionados à migração de disco
    * Propriedades adicionais nos objetos de extensão de VM e Imagem da Plataforma
* Azs.Fabric.Admin 
    * Novo cmdlet para adicionar nó de unidade de escala
* Azs.Backup.Admin
    * Set-AzsBackupShare agora é um alias para o cmdlet Set-AzsBackupConfiguration
    * Get-AzsBackupLocation agora é um alias para o cmdlet Get-AzsBackupConfiguration
    * Set-AzsBackupConfiguration, o parâmetro BackupShare agora é um alias para o caminho do parâmetro
* Azs.Subscriptions
    * Get-AzsDelegatedProviderOffer; o parâmetro OfferName agora é um alias para a oferta
* Azs.Subscriptions.Admin
    * Get-AzsDelegatedProviderOffer; o parâmetro OfferName agora é um alias para a oferta

## <a name="content"></a>Conteúdo:
### <a name="azure-bridge"></a>Azure Bridge
Versão prévia do módulo administrador do Azure Stack AzureBridge que permite distribuir imagens do Azure.

### <a name="backup"></a>Backup
Versão prévia do módulo administrador de Backup que permite aos administradores:
- Configurarem onde os backups são armazenados
- Executarem backups
- Listarem e restaurarem o backup completo

### <a name="commerce"></a>Comércio
Versão prévia do módulo administrador do Azure Stack Commerce que fornece uma maneira de exibir o uso de agregação de dados no sistema do Azure Stack.

### <a name="compute"></a>Computação
Versão prévia do módulo administrador do Azure Stack Compute que fornece funcionalidade para gerenciar cotas de computação, imagens da plataforma, discos gerenciados e extensões da máquina virtual.

### <a name="fabric"></a>Fabric
Versão prévia do módulo administrador do Azure Stack Fabric que permite que os administradores exibam e gerenciem os componentes de infraestrutura:
- Parar, Iniciar e Desligar os nós da unidade de escala
- Esvaziar e Retomar os nós da unidade de escala para as atividades relacionadas a FRU
- Reparar nós da unidade de escala
- Reinicializar função de Infraestrutura
- Parar, Iniciar e Desligar instâncias da função de Infraestrutura
- Criar novos Pools de IPs


### <a name="gallery"></a>Galeria
Versão prévia do módulo administrador do Azure Stack Gallery que fornece funcionalidade para gerenciar os itens da galeria no marketplace do Azure Stack.

### <a name="infrastructure-insights"></a>Infrastructure Insights
Versão prévia do módulo administrador do Infrastructure Insights que permite aos administradores:
- Exibirem a integridade de seus recursos de carimbo do Azure Stack
- Exibirem e gerenciarem alertas

### <a name="keyvault"></a>KeyVault
Versão prévia do módulo administrador do Azure Stack KeyVault que permite ao administrador exibir as cotas de KeyVault.

### <a name="network"></a>Rede
Versão prévia do módulo administrador da Rede que permite:
- Gerenciar as cotas de rede
- Exibir os recursos de rede alocados, como endereços IP públicos, redes virtuais, balanceadores de carga
- Fornecer um cmdlet que exibe uma visão geral do administrador

### <a name="storage"></a>Armazenamento
Versão prévia do módulo administrador do Armazenamento do Azure Stack.  Nessa versão, fornecemos funcionalidade para:
- Gerenciar as cotas de armazenamento
- Coletar o lixo dos recursos de armazenamento excluídos
- Restaurar as contas de armazenamento excluídas
- Migrar os contêineres de um compartilhamento para outro
- Exibir informações sobre os componentes de armazenamento individuais
- Exibir informações de uso e desempenho

### <a name="subscription-admin"></a>Administrador de assinatura
Versão prévia do módulo administrador de Assinatura do Azure Stack.  Esse módulo fornece funcionalidade para os administradores:
- Gerenciarem planos e ofertas
- Exibirem informações de uso e desempenho
- Gerenciar o RBAC

### <a name="subscription"></a>Assinatura
Versão prévia do módulo de Assinatura do Azure Stack.  Esse módulo fornece funcionalidade para os Usuários:
- Criar, Excluir e Atualizar Assinaturas

### <a name="update"></a>Atualizar
Versão prévia do módulo administrador de Atualização do Azure Stack.  Nesse módulo, os administradores podem:
- Listar e instalar as atualizações disponíveis
- Retomar as atualizações interrompidas
- Exibir as atualizações instaladas
