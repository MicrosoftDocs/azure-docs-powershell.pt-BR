---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946845"
---
# <span data-ttu-id="960ff-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="960ff-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="960ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="960ff-102">SYNOPSIS</span></span>
<span data-ttu-id="960ff-103">Retorna uma lista de aquisições de BLOB.</span><span class="sxs-lookup"><span data-stu-id="960ff-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="960ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="960ff-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="960ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="960ff-105">DESCRIPTION</span></span>
<span data-ttu-id="960ff-106">Retorna uma lista de aquisições de BLOB.</span><span class="sxs-lookup"><span data-stu-id="960ff-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="960ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="960ff-107">EXAMPLES</span></span>

### <span data-ttu-id="960ff-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="960ff-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="960ff-109">Obtenha a lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="960ff-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="960ff-110">OS</span><span class="sxs-lookup"><span data-stu-id="960ff-110">PARAMETERS</span></span>

### <span data-ttu-id="960ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="960ff-111">-DefaultProfile</span></span>
<span data-ttu-id="960ff-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="960ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="960ff-113">-Local</span><span class="sxs-lookup"><span data-stu-id="960ff-113">-Location</span></span>
<span data-ttu-id="960ff-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="960ff-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="960ff-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="960ff-115">-SubscriptionId</span></span>
<span data-ttu-id="960ff-116">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="960ff-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="960ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960ff-117">CommonParameters</span></span>
<span data-ttu-id="960ff-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="960ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960ff-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="960ff-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960ff-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="960ff-120">INPUTS</span></span>

## <span data-ttu-id="960ff-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="960ff-121">OUTPUTS</span></span>

### <span data-ttu-id="960ff-122">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="960ff-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="960ff-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="960ff-123">NOTES</span></span>

## <span data-ttu-id="960ff-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="960ff-124">RELATED LINKS</span></span>

