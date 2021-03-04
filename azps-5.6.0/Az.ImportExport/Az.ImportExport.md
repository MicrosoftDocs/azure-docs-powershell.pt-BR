---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: cce265bc3d61f445c6843b0c1ca340ad921e1089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888359"
---
# <span data-ttu-id="951ee-101">Módulo Az.ImportExport</span><span class="sxs-lookup"><span data-stu-id="951ee-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="951ee-102">Descrição</span><span class="sxs-lookup"><span data-stu-id="951ee-102">Description</span></span>
<span data-ttu-id="951ee-103">Microsoft Azure PowerShell: cmdlets ImportExport</span><span class="sxs-lookup"><span data-stu-id="951ee-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="951ee-104">Az.ImportExport Cmdlets</span><span class="sxs-lookup"><span data-stu-id="951ee-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="951ee-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="951ee-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="951ee-106">Obtém informações sobre um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="951ee-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="951ee-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="951ee-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="951ee-108">Retorna as Chaves do BitLocker para todas as unidades no trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="951ee-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="951ee-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="951ee-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="951ee-110">Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="951ee-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="951ee-111">Um local é uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="951ee-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="951ee-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="951ee-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="951ee-113">Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="951ee-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="951ee-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="951ee-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="951ee-115">Crie um objeto DriverList para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="951ee-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="951ee-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="951ee-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="951ee-117">Exclui um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="951ee-117">Deletes an existing job.</span></span>
<span data-ttu-id="951ee-118">Somente trabalhos nos estados Criando ou Concluído podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="951ee-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="951ee-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="951ee-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="951ee-120">Atualiza propriedades específicas de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="951ee-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="951ee-121">Você pode chamar essa operação para notificar o serviço de Importação/Exportação de que os discos rígidos que compõem o trabalho de importação ou exportação foram enviados para o data center da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="951ee-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="951ee-122">Ele também pode ser usado para cancelar um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="951ee-122">It can also be used to cancel an existing job.</span></span>

