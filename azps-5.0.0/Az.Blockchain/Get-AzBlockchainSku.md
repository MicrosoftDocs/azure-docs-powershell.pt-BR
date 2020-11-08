---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125493"
---
# <span data-ttu-id="6d0bc-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="6d0bc-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="6d0bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0bc-103">Lista as SKUs do tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="6d0bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d0bc-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6d0bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d0bc-105">DESCRIPTION</span></span>
<span data-ttu-id="6d0bc-106">Lista as SKUs do tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="6d0bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d0bc-107">EXAMPLES</span></span>

### <span data-ttu-id="6d0bc-108">Exemplo 1: listar a SKU para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="6d0bc-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="6d0bc-109">Este comando lista a SKU para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="6d0bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="6d0bc-110">PARAMETERS</span></span>

### <span data-ttu-id="6d0bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0bc-111">-DefaultProfile</span></span>
<span data-ttu-id="6d0bc-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d0bc-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d0bc-113">-SubscriptionId</span></span>
<span data-ttu-id="6d0bc-114">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6d0bc-115">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6d0bc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0bc-116">CommonParameters</span></span>
<span data-ttu-id="6d0bc-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d0bc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0bc-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d0bc-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0bc-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d0bc-119">INPUTS</span></span>

## <span data-ttu-id="6d0bc-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d0bc-120">OUTPUTS</span></span>

### <span data-ttu-id="6d0bc-121">Microsoft. Azure. PowerShell. cmdlets. Blockchain. Models. Api20180601Preview. IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="6d0bc-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="6d0bc-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d0bc-122">NOTES</span></span>

<span data-ttu-id="6d0bc-123">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6d0bc-123">ALIASES</span></span>

## <span data-ttu-id="6d0bc-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d0bc-124">RELATED LINKS</span></span>

