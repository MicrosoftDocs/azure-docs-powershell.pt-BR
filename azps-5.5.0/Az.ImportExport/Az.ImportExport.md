---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115296"
---
# <span data-ttu-id="e48fe-101">Módulo Az.ImportExport</span><span class="sxs-lookup"><span data-stu-id="e48fe-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="e48fe-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="e48fe-102">Description</span></span>
<span data-ttu-id="e48fe-103">Microsoft Azure PowerShell: cmdlets ImportExport</span><span class="sxs-lookup"><span data-stu-id="e48fe-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="e48fe-104">Az.ImportExport Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e48fe-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="e48fe-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e48fe-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="e48fe-106">Obtém informações sobre um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="e48fe-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="e48fe-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="e48fe-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="e48fe-108">Retorna as Teclas BitLocker para todas as unidades no trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="e48fe-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="e48fe-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="e48fe-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="e48fe-110">Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="e48fe-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="e48fe-111">Um local é uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="e48fe-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="e48fe-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e48fe-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="e48fe-113">Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e48fe-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="e48fe-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="e48fe-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="e48fe-115">Criar um Objeto de Lista de Driver para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="e48fe-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="e48fe-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e48fe-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="e48fe-117">Exclui um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="e48fe-117">Deletes an existing job.</span></span>
<span data-ttu-id="e48fe-118">Somente trabalhos nos estados Criar ou Concluído podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="e48fe-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="e48fe-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e48fe-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="e48fe-120">Atualiza as propriedades específicas de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="e48fe-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="e48fe-121">Você pode ligar para esta operação para notificar o serviço Importar/Exportar de que os discos rígidos compõem o trabalho de importação ou exportação que foram enviados para o data center da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e48fe-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="e48fe-122">Ele também pode ser usado para cancelar um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="e48fe-122">It can also be used to cancel an existing job.</span></span>

