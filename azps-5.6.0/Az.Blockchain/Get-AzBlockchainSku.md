---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: 9f33eef5b9f0bd0b245c444cf869fa0ff7a0a064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887821"
---
# <span data-ttu-id="b41ef-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="b41ef-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="b41ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b41ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b41ef-103">Lista os Skus do tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b41ef-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="b41ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b41ef-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b41ef-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b41ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b41ef-106">Lista os Skus do tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b41ef-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="b41ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b41ef-107">EXAMPLES</span></span>

### <span data-ttu-id="b41ef-108">Exemplo 1: Listar SKU para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="b41ef-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="b41ef-109">Este comando lista SKU para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b41ef-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="b41ef-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b41ef-110">PARAMETERS</span></span>

### <span data-ttu-id="b41ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41ef-111">-DefaultProfile</span></span>
<span data-ttu-id="b41ef-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b41ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b41ef-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b41ef-113">-SubscriptionId</span></span>
<span data-ttu-id="b41ef-114">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b41ef-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b41ef-115">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b41ef-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b41ef-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41ef-116">CommonParameters</span></span>
<span data-ttu-id="b41ef-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b41ef-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41ef-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b41ef-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41ef-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b41ef-119">INPUTS</span></span>

## <span data-ttu-id="b41ef-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b41ef-120">OUTPUTS</span></span>

### <span data-ttu-id="b41ef-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="b41ef-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="b41ef-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="b41ef-122">NOTES</span></span>

<span data-ttu-id="b41ef-123">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b41ef-123">ALIASES</span></span>

## <span data-ttu-id="b41ef-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b41ef-124">RELATED LINKS</span></span>

