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
# <a name="azure-stack-module-170"></a><span data-ttu-id="64d0f-103">Módulo do Azure Stack 1.7.0</span><span class="sxs-lookup"><span data-stu-id="64d0f-103">Azure Stack Module 1.7.0</span></span>

## <a name="requirements"></a><span data-ttu-id="64d0f-104">Requisitos:</span><span class="sxs-lookup"><span data-stu-id="64d0f-104">Requirements:</span></span>
<span data-ttu-id="64d0f-105">a versão mínima do Azure Stack com suporte é a 1901.</span><span class="sxs-lookup"><span data-stu-id="64d0f-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="64d0f-106">Observação: caso esteja usando uma versão anterior, instale a versão 1.7.0</span><span class="sxs-lookup"><span data-stu-id="64d0f-106">Note: If you are using an earlier version install version 1.7.0</span></span>

## <a name="install"></a><span data-ttu-id="64d0f-107">Instalar</span><span class="sxs-lookup"><span data-stu-id="64d0f-107">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="64d0f-108">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="64d0f-108">Release Notes</span></span>
* <span data-ttu-id="64d0f-109">Com suporte com a atualização 1901</span><span class="sxs-lookup"><span data-stu-id="64d0f-109">Supported with 1901 update</span></span>
* <span data-ttu-id="64d0f-110">Essa é uma versão com alteração de falhas.</span><span class="sxs-lookup"><span data-stu-id="64d0f-110">This a breaking change release.</span></span> <span data-ttu-id="64d0f-111">Para obter detalhes sobre as alterações de falhas, confira https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="64d0f-111">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="64d0f-112">Alteração de falha do módulo Azs.Backup.Admin \*: Alterações de backup do modo de criptografia baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="64d0f-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="64d0f-113">O suporte para chaves simétricas está preterido.</span><span class="sxs-lookup"><span data-stu-id="64d0f-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="64d0f-114">Azs.Fabric.Admin Module       \* Preterido          \* Get-AzsInfrastructureVolume foi preterido; fornecemos o novo cmdlet Get-AzsVolume           \* Get-AzsStorageSystem foi preterido; fornecemos o novo cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool foi preterido; o novo objeto StorageSubSystem tem a propriedade de capacidade</span><span class="sxs-lookup"><span data-stu-id="64d0f-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="64d0f-115">Azs.Compute.Admin Module           \* Correção de bug: Add-AzsPlatformImage, Get-AzsPlatformImage: Chamar ConvertTo-PlatformImageObject somente no caminho bem-sucedido           \* Correção de bug: Add-AzsVmExtension, Get-AzsVmExtension: Chamar ConvertTo-VmExtensionObject somente no caminho bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="64d0f-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="64d0f-116">Módulo Azs.Storage.Admin           \* Correção de bug – Nova Cota de Armazenamento usa os padrões se nenhum for fornecido.'</span><span class="sxs-lookup"><span data-stu-id="64d0f-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>

