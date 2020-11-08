---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117369"
---
# <span data-ttu-id="c2a08-101">Módulo AZ. ImportExport</span><span class="sxs-lookup"><span data-stu-id="c2a08-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="c2a08-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="c2a08-102">Description</span></span>
<span data-ttu-id="c2a08-103">Microsoft Azure PowerShell: cmdlets do ImportExport</span><span class="sxs-lookup"><span data-stu-id="c2a08-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="c2a08-104">Cmdlets AZ. ImportExport</span><span class="sxs-lookup"><span data-stu-id="c2a08-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="c2a08-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="c2a08-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="c2a08-106">Obtém informações sobre um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="c2a08-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="c2a08-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="c2a08-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="c2a08-108">Retorna as chaves BitLocker para todas as unidades no trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="c2a08-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="c2a08-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="c2a08-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="c2a08-110">Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="c2a08-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="c2a08-111">Um local é uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a08-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="c2a08-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="c2a08-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="c2a08-113">Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="c2a08-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="c2a08-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="c2a08-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="c2a08-115">Crie um objeto Driverlist para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="c2a08-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="c2a08-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="c2a08-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="c2a08-117">Exclui um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="c2a08-117">Deletes an existing job.</span></span>
<span data-ttu-id="c2a08-118">Somente os trabalhos nos Estados criando ou concluídos podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="c2a08-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="c2a08-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="c2a08-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="c2a08-120">Atualiza propriedades específicas de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="c2a08-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="c2a08-121">Você pode chamar essa operação para notificar o serviço de importação/exportação de que os discos rígidos que compõem o trabalho de importação ou de exportação foram enviados para o Data Center da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2a08-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="c2a08-122">Ele também pode ser usado para cancelar um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="c2a08-122">It can also be used to cancel an existing job.</span></span>

