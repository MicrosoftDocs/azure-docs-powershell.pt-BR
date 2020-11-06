---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 74c358935efff57f2caf9fb7b6bd8b75e429aeab
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425462"
---
# <span data-ttu-id="d1e3e-101">Módulo AZS. COMPUTE. admin</span><span class="sxs-lookup"><span data-stu-id="d1e3e-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="d1e3e-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="d1e3e-102">Description</span></span>
<span data-ttu-id="d1e3e-103">Versão prévia do módulo AzureStack Compute Operator, que fornece funcionalidade para gerenciar cotas de computação, imagens de plataforma e extensões de máquina virtual, bem como trabalhos de migração de discos gerenciados para rebalancear o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-103">Preview release of the AzureStack Compute operator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="d1e3e-104">Cmdlets do AZS. COMPUTE. admin</span><span class="sxs-lookup"><span data-stu-id="d1e3e-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="d1e3e-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d1e3e-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="d1e3e-106">Adicionar uma imagem de plataforma da máquina virtual a partir de uma determinada configuração de imagem.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="d1e3e-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="d1e3e-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="d1e3e-108">Crie uma nova imagem de extensão de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="d1e3e-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d1e3e-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="d1e3e-110">Retorna as cotas que especificam os limites de cota para objetos de computação.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="d1e3e-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="d1e3e-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="d1e3e-112">Retorna a lista de discos gerenciados que podem ser migrados no compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="d1e3e-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d1e3e-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="d1e3e-114">Retorna a lista de trabalhos de migração de disco gerenciados.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="d1e3e-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d1e3e-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="d1e3e-116">Retorna as imagens da máquina virtual carregadas no repositório de imagens da plataforma.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="d1e3e-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="d1e3e-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="d1e3e-118">Retorna as extensões de imagem de máquina virtual disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="d1e3e-119">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d1e3e-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="d1e3e-120">Crie uma nova cota de computação usada para limitar os recursos de computação.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="d1e3e-121">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d1e3e-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="d1e3e-122">Inicia um trabalho de migração de disco gerenciado para migrar discos gerenciados para o compartilhamento de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="d1e3e-123">Novo-datadiskobject</span><span class="sxs-lookup"><span data-stu-id="d1e3e-123">New-DataDiskObject</span></span>](New-DataDiskObject.md)
<span data-ttu-id="d1e3e-124">Cria um disco de dados que é usado para criar uma nova imagem da plataforma da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="d1e3e-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d1e3e-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="d1e3e-126">Exclui a cota de computação especificada.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="d1e3e-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d1e3e-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="d1e3e-128">Exclua uma imagem de máquina virtual do repositório de imagens da plataforma.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="d1e3e-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="d1e3e-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="d1e3e-130">Exclui uma imagem de extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="d1e3e-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d1e3e-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="d1e3e-132">Atualize uma cota de computação existente usando os parâmetros fornecidos.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="d1e3e-133">Parar-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d1e3e-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="d1e3e-134">Cancelar um trabalho de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d1e3e-134">Cancel a managed disk migration job.</span></span>

