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
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152892"
---
# <a name="azure-stack-module-160"></a>Módulo do Azure Stack 1.6.0

## <a name="requirements"></a>Requisitos:
A versão mínima do Azure Stack com suporte é 1811.

Observação: Se você estiver usando uma versão anterior, instale a versão 1.6.0

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

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Notas de versão
* Com suporte com a atualização 1811
* Módulo Azs.Compute.Admin
    * Correção do prefixo Azs ausente para New-DataDiskObject e adição de alias com aviso de reprovação futura.
* Módulo Azs.Update.Admin
    * Adição de um aviso para recomendar a execução do Test-AzureStack antes do Install-AzsUpdate
* Azs.Fabric.Admin
    * Novo cmdlet (o Azure Stack 1811 ou superior tem suporte para os recursos)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Reprovação
        * Agora Get-AzsInfrastructureVolume é um alias para o cmdlet Get-AzsVolume
* Azs.InfrastructureInsights.Admin
    *  Adição de um novo cmdlet Repair-AzsAlert
* Azs.Storage.Admin
    * Correção de bug onde não estão sendo usados valores de cota padrão
* Módulo Azs.Subscriptions.Admin
    * Correção do prefixo Azs ausente para New-AddonPlanDefinitionObject e adição de alias com aviso de reprovação futura.
