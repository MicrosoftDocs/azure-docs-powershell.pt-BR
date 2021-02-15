---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114270"
---
# <span data-ttu-id="61989-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="61989-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="61989-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61989-102">SYNOPSIS</span></span>
<span data-ttu-id="61989-103">Obter lista de lojas particulares</span><span class="sxs-lookup"><span data-stu-id="61989-103">Get private store list</span></span>

## <span data-ttu-id="61989-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61989-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61989-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="61989-105">DESCRIPTION</span></span>
<span data-ttu-id="61989-106">Obter a lista de lojas particulares que foram criadas sob o escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="61989-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="61989-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61989-107">EXAMPLES</span></span>

### <span data-ttu-id="61989-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61989-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="61989-109">lista de lojas particulares que foram criadas sob o escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="61989-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="61989-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61989-110">PARAMETERS</span></span>

### <span data-ttu-id="61989-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61989-111">-DefaultProfile</span></span>
<span data-ttu-id="61989-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61989-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61989-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61989-113">CommonParameters</span></span>
<span data-ttu-id="61989-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61989-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61989-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61989-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61989-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="61989-116">INPUTS</span></span>

### <span data-ttu-id="61989-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61989-117">None</span></span>

## <span data-ttu-id="61989-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="61989-118">OUTPUTS</span></span>

### <span data-ttu-id="61989-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="61989-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="61989-120">Notas</span><span class="sxs-lookup"><span data-stu-id="61989-120">NOTES</span></span>

## <span data-ttu-id="61989-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61989-121">RELATED LINKS</span></span>
