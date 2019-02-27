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
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240502"
---
# <a name="azure-stack-module-170"></a>Módulo do Azure Stack 1.7.0

## <a name="requirements"></a>Requisitos:
a versão mínima do Azure Stack com suporte é a 1901.

Observação: caso esteja usando uma versão anterior, instale a versão 1.7.0

## <a name="install"></a>Instalar
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a>Notas de versão
* Com suporte com a atualização 1901
* Essa é uma versão com alteração de falhas. Para obter detalhes sobre as alterações de falhas, confira https://aka.ms/azspshmigration170
* Alteração de falha do módulo Azs.Backup.Admin *: Alterações de backup do modo de criptografia baseada em certificado. O suporte para chaves simétricas está preterido.
* Azs.Fabric.Admin Module       * Preterido          * Get-AzsInfrastructureVolume foi preterido; fornecemos o novo cmdlet Get-AzsVolume           * Get-AzsStorageSystem foi preterido; fornecemos o novo cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool foi preterido; o novo objeto StorageSubSystem tem a propriedade de capacidade
* Azs.Compute.Admin Module           * Correção de bug: Add-AzsPlatformImage, Get-AzsPlatformImage: Chamar ConvertTo-PlatformImageObject somente no caminho bem-sucedido           * Correção de bug: Add-AzsVmExtension, Get-AzsVmExtension: Chamar ConvertTo-VmExtensionObject somente no caminho bem-sucedido
* Módulo Azs.Storage.Admin           * Correção de bug – Nova Cota de Armazenamento usa os padrões se nenhum for fornecido.'

