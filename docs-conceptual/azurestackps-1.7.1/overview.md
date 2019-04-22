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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58808046"
---
# <a name="azure-stack-module-171"></a>Módulo do Azure Stack 1.7.1

## <a name="requirements"></a>Requisitos:

a versão mínima do Azure Stack com suporte é a 1901.

Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalar

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Notas de versão

* Com suporte com a atualização 1901
* Essa é uma versão com alteração de falhas. Para obter detalhes sobre as alterações de falhas, confira <https://aka.ms/azspshmigration170>
* Alteração de falha do módulo Azs.Backup.Admin *: Alterações de backup do modo de criptografia baseada em certificado. O suporte para chaves simétricas está preterido.
* Azs.Fabric.Admin Module       * Preterido          * Get-AzsInfrastructureVolume foi preterido; fornecemos o novo cmdlet Get-AzsVolume           * Get-AzsStorageSystem foi preterido; fornecemos o novo cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool foi preterido; o novo objeto StorageSubSystem tem a propriedade de capacidade
* Azs.Compute.Admin Module           * Correção de bug: Add-AzsPlatformImage, Get-AzsPlatformImage: Chamar ConvertTo-PlatformImageObject somente no caminho bem-sucedido           * Correção de bug: Add-AzsVmExtension, Get-AzsVmExtension: Chamar ConvertTo-VmExtensionObject somente no caminho bem-sucedido
* Módulo Azs.Storage.Admin           * Correção de bug – Nova Cota de Armazenamento usa os padrões se nenhum for fornecido.'
