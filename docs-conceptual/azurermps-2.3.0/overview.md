---
title: Visão geral do Azure Stack PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack PowerShell com instruções de instalação e configuração.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178452"
---
# <a name="azurerm-module-230"></a>Módulo do AzureRM 2.3.0

## <a name="requirements"></a>Requisitos:
A versão mínima do Azure Stack com suporte é 1808.

Nota: se você estiver usando uma versão anterior, instale a versão 1.2.11


## <a name="install"></a>Instalar
```powershell
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

##<a name="release-notes"></a>Notas de versão
* A versão 2.3.0 vem com uma lista de alterações significativas. Para atualizar a partir da versão 1.2.11, criamos um guia de migração em https://aka.ms/azspowershellmigration
* Essa versão corresponde ao perfil de API específico do Azure Stack 2018-03-01-hybrid
* Todos os módulos estão usando dependências maior que ou igual a no módulo AzureRM.Profile.
* As versões de API com suporte por cada um dos módulos são atualizadas. 
    * Computação - 2017-03-30
    * Rede - 2017-10-01
    * Armazenamento - 2016-01-01
    * Recursos - 2018-02-01
    * Keyvault - 2016-10-01
    * DNS - 2016-04-01
* O mapa de versão de API completo para cada um dos tipos de recursos pode ser encontrado em https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json

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
