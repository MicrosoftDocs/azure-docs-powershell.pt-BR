---
title: Visão geral do Azure Stack Hub Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Hub Admin PowerShell com instruções de instalação e de configuração.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: ec4591e4f44fa56b7482d2dec3f525cb02dbd94b
ms.sourcegitcommit: a24069b411d3a6011067770430b6dcdd4b2c2159
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/16/2020
ms.locfileid: "97532252"
---
# <a name="azure-stack-hub-module-202"></a>Módulo do Azure Stack Hub 2.0.2

## <a name="requirements"></a>Requisitos:

A versão mínima do Azure Stack Hub compatível é a 2002.

Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalar

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease -SkipPublisherCheck

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a>Notas de versão

* Compatível com a atualização 2002.  

  O Azure Stack Hub 2.0.0 é uma alteração da falha. O módulo usa o módulo Az em vez do AzureRM. Você pode encontrar um guia de migração e uma lista de alterações da falha em [Migrar do AzureRM para o Azure PowerShell Az no Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).
