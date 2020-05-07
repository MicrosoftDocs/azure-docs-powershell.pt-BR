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
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "78264403"
---
# <a name="azure-stack-module-180"></a><span data-ttu-id="a54fc-103">Módulo do Azure Stack 1.8.0</span><span class="sxs-lookup"><span data-stu-id="a54fc-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="a54fc-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="a54fc-104">Requirements:</span></span>

<span data-ttu-id="a54fc-105">A versão mínima do Azure Stack compatível é a 1910.</span><span class="sxs-lookup"><span data-stu-id="a54fc-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="a54fc-106">Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="a54fc-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="a54fc-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="a54fc-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="a54fc-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="a54fc-108">Release Notes</span></span>

* <span data-ttu-id="a54fc-109">Compatível com a atualização 1910</span><span class="sxs-lookup"><span data-stu-id="a54fc-109">Supported with 1910 update</span></span>
* <span data-ttu-id="a54fc-110">As alterações incluem:</span><span class="sxs-lookup"><span data-stu-id="a54fc-110">Changes include:</span></span>

    - <span data-ttu-id="a54fc-111">**Novo módulo de administrador de DRP**: O DRP (provedor de recursos de implantação) permite implantações orquestradas de provedores de recursos para o Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="a54fc-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="a54fc-112">Esses comandos interagem com a camada de Azure Resource Manager para interagir com o DRP.</span><span class="sxs-lookup"><span data-stu-id="a54fc-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="a54fc-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="a54fc-113">**BRP**:</span></span>
        - <span data-ttu-id="a54fc-114">Suporte para restauração de função única para backup de infraestrutura do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="a54fc-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="a54fc-115">Adicione o parâmetro `RoleName` ao cmdlet do R`estore-AzsBackup`.</span><span class="sxs-lookup"><span data-stu-id="a54fc-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="a54fc-116">**FRP**: Alterações da falha para recursos de **unidade** e de **volume** com a versão de API de 01/05/2019.</span><span class="sxs-lookup"><span data-stu-id="a54fc-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="a54fc-117">Os recursos são compatíveis com o Azure Stack Hub 1910 e versões posteriores:</span><span class="sxs-lookup"><span data-stu-id="a54fc-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="a54fc-118">Os valores de ID, `Name`, `HealthStatus` e `OperationalStatus` foram alterados.</span><span class="sxs-lookup"><span data-stu-id="a54fc-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="a54fc-119">Novas propriedades `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` e `StoragePool` compatíveis com recursos de **unidade**.</span><span class="sxs-lookup"><span data-stu-id="a54fc-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="a54fc-120">As propriedades `CanPool` e `CannotPoolReason` de recursos de **unidade** foram preteridas; em vez disso, use `OperationalStatus`.</span><span class="sxs-lookup"><span data-stu-id="a54fc-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
