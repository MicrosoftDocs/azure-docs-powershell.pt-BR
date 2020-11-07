---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946751"
---
# <span data-ttu-id="e5931-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="e5931-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="e5931-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5931-102">SYNOPSIS</span></span>
<span data-ttu-id="e5931-103">Retorna as configurações do provedor de recursos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5931-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="e5931-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5931-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5931-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5931-105">DESCRIPTION</span></span>
<span data-ttu-id="e5931-106">Retorna as configurações do provedor de recursos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5931-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="e5931-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5931-107">EXAMPLES</span></span>

### <span data-ttu-id="e5931-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="e5931-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="e5931-109">Obter as configurações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e5931-109">Get the storage settings.</span></span>

## <span data-ttu-id="e5931-110">OS</span><span class="sxs-lookup"><span data-stu-id="e5931-110">PARAMETERS</span></span>

### <span data-ttu-id="e5931-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5931-111">-DefaultProfile</span></span>
<span data-ttu-id="e5931-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5931-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5931-113">-Local</span><span class="sxs-lookup"><span data-stu-id="e5931-113">-Location</span></span>
<span data-ttu-id="e5931-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e5931-114">Resource location.</span></span>

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

### <span data-ttu-id="e5931-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5931-115">-SubscriptionId</span></span>
<span data-ttu-id="e5931-116">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e5931-116">Subscription Id.</span></span>

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

### <span data-ttu-id="e5931-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5931-117">CommonParameters</span></span>
<span data-ttu-id="e5931-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5931-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5931-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5931-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5931-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5931-120">INPUTS</span></span>

## <span data-ttu-id="e5931-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5931-121">OUTPUTS</span></span>

### <span data-ttu-id="e5931-122">Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="e5931-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="e5931-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5931-123">NOTES</span></span>

## <span data-ttu-id="e5931-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5931-124">RELATED LINKS</span></span>

