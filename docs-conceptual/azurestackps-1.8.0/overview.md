---
title: Visão geral do Azure Stack Admin PowerShell | Microsoft Docs
description: Uma visão geral do Azure Stack Admin PowerShell com instruções de instalação e configuração.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: e19fea440025e7a00a037e360ac95ff8e0e62129
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96428003"
---
# <a name="azure-stack-module-180"></a>Módulo do Azure Stack 1.8.0

## <a name="requirements"></a>Requisitos:

A versão mínima do Azure Stack compatível é a 1910.

Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Instalar

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Notas de versão

* Compatível com a atualização 1910
* Alterações incluem:

    - **Novo módulo de administrador de DRP**: O DRP (provedor de recursos de implantação) permite implantações orquestradas de provedores de recursos para o Azure Stack Hub. Esses comandos interagem com a camada de Azure Resource Manager para interagir com o DRP.

    - **BRP**:
        - Suporte para restauração de função única para backup de infraestrutura do Azure Stack.
        - Adicione o parâmetro `RoleName` ao cmdlet do R`estore-AzsBackup`.

    - **FRP**: Alterações da falha para recursos de **unidade** e de **volume** com a versão de API de 01/05/2019. Os recursos são compatíveis com o Azure Stack Hub 1910 e versões posteriores:
        - Os valores de ID, `Name`, `HealthStatus` e `OperationalStatus` foram alterados.
        - Novas propriedades `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` e `StoragePool` compatíveis com recursos de **unidade**.
        - As propriedades `CanPool` e `CannotPoolReason` de recursos de **unidade** foram preteridas; em vez disso, use `OperationalStatus`.