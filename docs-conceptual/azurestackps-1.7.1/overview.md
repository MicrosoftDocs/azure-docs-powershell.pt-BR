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
ms.sourcegitcommit: d3069aba7d1ac248aff755e4b21533af1f73251d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58808046"
---
# <a name="azure-stack-module-171"></a><span data-ttu-id="fb4e7-103">Módulo do Azure Stack 1.7.1</span><span class="sxs-lookup"><span data-stu-id="fb4e7-103">Azure Stack Module 1.7.1</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4e7-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="fb4e7-104">Requirements:</span></span>

<span data-ttu-id="fb4e7-105">a versão mínima do Azure Stack com suporte é a 1901.</span><span class="sxs-lookup"><span data-stu-id="fb4e7-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="fb4e7-106">Observação: Para as versões anteriores de verificação do Azure Stack [Instalar o Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="fb4e7-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="fb4e7-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="fb4e7-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a><span data-ttu-id="fb4e7-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="fb4e7-108">Release Notes</span></span>

* <span data-ttu-id="fb4e7-109">Com suporte com a atualização 1901</span><span class="sxs-lookup"><span data-stu-id="fb4e7-109">Supported with 1901 update</span></span>
* <span data-ttu-id="fb4e7-110">Essa é uma versão com alteração de falhas.</span><span class="sxs-lookup"><span data-stu-id="fb4e7-110">This a breaking change release.</span></span> <span data-ttu-id="fb4e7-111">Para obter detalhes sobre as alterações de falhas, confira <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="fb4e7-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="fb4e7-112">Alteração de falha do módulo Azs.Backup.Admin \*: Alterações de backup do modo de criptografia baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="fb4e7-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="fb4e7-113">O suporte para chaves simétricas está preterido.</span><span class="sxs-lookup"><span data-stu-id="fb4e7-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="fb4e7-114">Azs.Fabric.Admin Module       \* Preterido          \* Get-AzsInfrastructureVolume foi preterido; fornecemos o novo cmdlet Get-AzsVolume           \* Get-AzsStorageSystem foi preterido; fornecemos o novo cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool foi preterido; o novo objeto StorageSubSystem tem a propriedade de capacidade</span><span class="sxs-lookup"><span data-stu-id="fb4e7-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="fb4e7-115">Azs.Compute.Admin Module           \* Correção de bug: Add-AzsPlatformImage, Get-AzsPlatformImage: Chamar ConvertTo-PlatformImageObject somente no caminho bem-sucedido           \* Correção de bug: Add-AzsVmExtension, Get-AzsVmExtension: Chamar ConvertTo-VmExtensionObject somente no caminho bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fb4e7-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="fb4e7-116">Módulo Azs.Storage.Admin           \* Correção de bug – Nova Cota de Armazenamento usa os padrões se nenhum for fornecido.'</span><span class="sxs-lookup"><span data-stu-id="fb4e7-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
