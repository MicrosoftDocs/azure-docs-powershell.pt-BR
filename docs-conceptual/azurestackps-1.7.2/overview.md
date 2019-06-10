---
title: Visão geral do Azure Stack Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Admin PowerShell com instruções de instalação e configuração.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855781"
---
# <a name="azure-stack-module-172"></a>Módulo do Azure Stack 1.7.2

## <a name="requirements"></a>Requisitos:

A versão mínima do Azure Stack compatível é a 1904.

Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install-powershell-for-azure-stack"></a>Instalar o PowerShell para o Azure Stack

A instalação tem três etapas:

1. Instalar o Azure Stack PowerShell dependendo da versão do Azure Stack
2. Habilitar recursos de armazenamento adicionais
3. Confirmar a instalação do PowerShell

### <a name="install-azure-stack-powershell"></a>Instalar o PowerShell do Azure Stack

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a>Habilitar recursos de armazenamento adicionais

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a>Notas de versão

* Compatível com a atualização 1904
* Essa é uma versão com alteração de falhas. Para obter detalhes sobre as alterações de falhas, confira <https://aka.ms/azspshmigration170>
* Alteração de falha do módulo Azs.Backup.Admin *: Alterações de backup do modo de criptografia baseada em certificado. O suporte para chaves simétricas está preterido.
* Azs.Fabric.Admin Module       * Preterido          * Get-AzsInfrastructureVolume foi preterido; fornecemos o novo cmdlet Get-AzsVolume           * Get-AzsStorageSystem foi preterido; fornecemos o novo cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool foi preterido; o novo objeto StorageSubSystem tem a propriedade de capacidade
* Azs.Compute.Admin Module           * Correção de bug: Add-AzsPlatformImage, Get-AzsPlatformImage: Chamar ConvertTo-PlatformImageObject somente no caminho bem-sucedido           * Correção de bug: Add-AzsVmExtension, Get-AzsVmExtension: Chamar ConvertTo-VmExtensionObject somente no caminho bem-sucedido
* Módulo Azs.Storage.Admin           * Correção de bug – Nova Cota de Armazenamento usa os padrões se nenhum for fornecido.'
