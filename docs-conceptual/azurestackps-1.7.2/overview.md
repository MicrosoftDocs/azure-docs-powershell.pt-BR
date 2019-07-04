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
ms.openlocfilehash: b77e09f6fcd5b7752af9f51a42d357db4f1b13db
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037679"
---
# <a name="azure-stack-module-172"></a>Módulo do Azure Stack 1.7.2

## <a name="requirements"></a>Requisitos:

A versão mínima do Azure Stack compatível é a 1904.

Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalar

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Notas de versão

* Compatível com a atualização 1904
* Essa é uma versão com alteração de falhas. Para obter detalhes sobre as alterações de falhas, confira <https://aka.ms/azspshmigration170>
* Alterações da falha: Alterações de backup do modo de criptografia baseada em certificado. O suporte para chaves simétricas está preterido.
* Para obter detalhes sobre as alterações de falhas, confira https://aka.ms/azspshmigration170
* Módulo Azs.Storage.Admin 
* Correção de bug – Nova Cota de Armazenamento usará os padrões se nenhum for fornecido.
