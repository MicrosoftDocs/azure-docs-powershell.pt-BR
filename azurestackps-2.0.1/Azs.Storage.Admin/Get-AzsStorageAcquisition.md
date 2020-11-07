---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945261"
---
# <span data-ttu-id="0c085-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="0c085-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="0c085-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c085-102">SYNOPSIS</span></span>
<span data-ttu-id="0c085-103">Retorna uma lista de aquisições de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0c085-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="0c085-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c085-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c085-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c085-105">DESCRIPTION</span></span>
<span data-ttu-id="0c085-106">Retorna uma lista de aquisições de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0c085-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="0c085-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c085-107">EXAMPLES</span></span>

### <span data-ttu-id="0c085-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="0c085-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="0c085-109">Obtenha a lista de Acquistions de BLOB.</span><span class="sxs-lookup"><span data-stu-id="0c085-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="0c085-110">OS</span><span class="sxs-lookup"><span data-stu-id="0c085-110">PARAMETERS</span></span>

### <span data-ttu-id="0c085-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c085-111">-DefaultProfile</span></span>
<span data-ttu-id="0c085-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c085-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c085-113">-Local</span><span class="sxs-lookup"><span data-stu-id="0c085-113">-Location</span></span>
<span data-ttu-id="0c085-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="0c085-114">Resource location.</span></span>

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

### <span data-ttu-id="0c085-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c085-115">-SubscriptionId</span></span>
<span data-ttu-id="0c085-116">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0c085-116">Subscription Id.</span></span>

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

### <span data-ttu-id="0c085-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c085-117">CommonParameters</span></span>
<span data-ttu-id="0c085-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c085-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c085-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c085-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c085-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c085-120">INPUTS</span></span>

## <span data-ttu-id="0c085-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c085-121">OUTPUTS</span></span>

### <span data-ttu-id="0c085-122">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="0c085-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="0c085-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c085-123">NOTES</span></span>

## <span data-ttu-id="0c085-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c085-124">RELATED LINKS</span></span>

