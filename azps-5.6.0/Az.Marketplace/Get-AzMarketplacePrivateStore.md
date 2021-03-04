---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: 2dd2ec778a64403b9f13cd923e7b7312e72a6c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892128"
---
# <span data-ttu-id="f0143-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="f0143-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="f0143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0143-102">SYNOPSIS</span></span>
<span data-ttu-id="f0143-103">Obter lista de lojas privadas</span><span class="sxs-lookup"><span data-stu-id="f0143-103">Get private store list</span></span>

## <span data-ttu-id="f0143-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f0143-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0143-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f0143-105">DESCRIPTION</span></span>
<span data-ttu-id="f0143-106">Obter lista de lojas privadas que foram criadas em escopo de locatário</span><span class="sxs-lookup"><span data-stu-id="f0143-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="f0143-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0143-107">EXAMPLES</span></span>

### <span data-ttu-id="f0143-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0143-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="f0143-109">lista de lojas privadas que foram criadas em escopo de locatário</span><span class="sxs-lookup"><span data-stu-id="f0143-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="f0143-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f0143-110">PARAMETERS</span></span>

### <span data-ttu-id="f0143-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0143-111">-DefaultProfile</span></span>
<span data-ttu-id="f0143-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0143-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0143-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0143-113">CommonParameters</span></span>
<span data-ttu-id="f0143-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0143-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0143-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0143-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0143-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0143-116">INPUTS</span></span>

### <span data-ttu-id="f0143-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f0143-117">None</span></span>

## <span data-ttu-id="f0143-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f0143-118">OUTPUTS</span></span>

### <span data-ttu-id="f0143-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="f0143-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="f0143-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="f0143-120">NOTES</span></span>

## <span data-ttu-id="f0143-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0143-121">RELATED LINKS</span></span>
