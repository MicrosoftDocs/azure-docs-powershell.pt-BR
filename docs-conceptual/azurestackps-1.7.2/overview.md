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
# <a name="azure-stack-module-172"></a><span data-ttu-id="123e9-103">Módulo do Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="123e9-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="123e9-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="123e9-104">Requirements:</span></span>

<span data-ttu-id="123e9-105">A versão mínima do Azure Stack compatível é a 1904.</span><span class="sxs-lookup"><span data-stu-id="123e9-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="123e9-106">Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="123e9-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="123e9-107">Instalar o PowerShell para o Azure Stack</span><span class="sxs-lookup"><span data-stu-id="123e9-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="123e9-108">A instalação tem três etapas:</span><span class="sxs-lookup"><span data-stu-id="123e9-108">Installation has three steps:</span></span>

1. <span data-ttu-id="123e9-109">Instalar o Azure Stack PowerShell dependendo da versão do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="123e9-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="123e9-110">Habilitar recursos de armazenamento adicionais</span><span class="sxs-lookup"><span data-stu-id="123e9-110">Enable additional storage features</span></span>
3. <span data-ttu-id="123e9-111">Confirmar a instalação do PowerShell</span><span class="sxs-lookup"><span data-stu-id="123e9-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="123e9-112">Instalar o PowerShell do Azure Stack</span><span class="sxs-lookup"><span data-stu-id="123e9-112">Install Azure Stack PowerShell</span></span>

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

### <a name="enable-additional-storage-features"></a><span data-ttu-id="123e9-113">Habilitar recursos de armazenamento adicionais</span><span class="sxs-lookup"><span data-stu-id="123e9-113">Enable additional storage features</span></span>

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

## <a name="release-notes"></a><span data-ttu-id="123e9-114">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="123e9-114">Release Notes</span></span>

* <span data-ttu-id="123e9-115">Compatível com a atualização 1904</span><span class="sxs-lookup"><span data-stu-id="123e9-115">Supported with 1904 update</span></span>
* <span data-ttu-id="123e9-116">Essa é uma versão com alteração de falhas.</span><span class="sxs-lookup"><span data-stu-id="123e9-116">This a breaking change release.</span></span> <span data-ttu-id="123e9-117">Para obter detalhes sobre as alterações de falhas, confira <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="123e9-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="123e9-118">Alteração de falha do módulo Azs.Backup.Admin \*: Alterações de backup do modo de criptografia baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="123e9-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="123e9-119">O suporte para chaves simétricas está preterido.</span><span class="sxs-lookup"><span data-stu-id="123e9-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="123e9-120">Azs.Fabric.Admin Module       \* Preterido          \* Get-AzsInfrastructureVolume foi preterido; fornecemos o novo cmdlet Get-AzsVolume           \* Get-AzsStorageSystem foi preterido; fornecemos o novo cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool foi preterido; o novo objeto StorageSubSystem tem a propriedade de capacidade</span><span class="sxs-lookup"><span data-stu-id="123e9-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="123e9-121">Azs.Compute.Admin Module           \* Correção de bug: Add-AzsPlatformImage, Get-AzsPlatformImage: Chamar ConvertTo-PlatformImageObject somente no caminho bem-sucedido           \* Correção de bug: Add-AzsVmExtension, Get-AzsVmExtension: Chamar ConvertTo-VmExtensionObject somente no caminho bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="123e9-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="123e9-122">Módulo Azs.Storage.Admin           \* Correção de bug – Nova Cota de Armazenamento usa os padrões se nenhum for fornecido.'</span><span class="sxs-lookup"><span data-stu-id="123e9-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
