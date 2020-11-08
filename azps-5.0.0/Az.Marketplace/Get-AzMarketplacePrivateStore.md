---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124581"
---
# <span data-ttu-id="5dbc9-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="5dbc9-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="5dbc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5dbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbc9-103">Obter lista da loja particular</span><span class="sxs-lookup"><span data-stu-id="5dbc9-103">Get private store list</span></span>

## <span data-ttu-id="5dbc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5dbc9-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dbc9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5dbc9-105">DESCRIPTION</span></span>
<span data-ttu-id="5dbc9-106">Obter lista de repositório particular que foi criada em escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="5dbc9-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="5dbc9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5dbc9-107">EXAMPLES</span></span>

### <span data-ttu-id="5dbc9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5dbc9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="5dbc9-109">lista de repositório particular que foi criada em escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="5dbc9-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="5dbc9-110">OS</span><span class="sxs-lookup"><span data-stu-id="5dbc9-110">PARAMETERS</span></span>

### <span data-ttu-id="5dbc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbc9-111">-DefaultProfile</span></span>
<span data-ttu-id="5dbc9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5dbc9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbc9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbc9-113">CommonParameters</span></span>
<span data-ttu-id="5dbc9-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dbc9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbc9-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dbc9-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbc9-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5dbc9-116">INPUTS</span></span>

### <span data-ttu-id="5dbc9-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5dbc9-117">None</span></span>

## <span data-ttu-id="5dbc9-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5dbc9-118">OUTPUTS</span></span>

### <span data-ttu-id="5dbc9-119">Microsoft. Azure. Commands. marketplace. Models. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="5dbc9-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="5dbc9-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5dbc9-120">NOTES</span></span>

## <span data-ttu-id="5dbc9-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5dbc9-121">RELATED LINKS</span></span>
