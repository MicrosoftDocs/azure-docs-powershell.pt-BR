---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: 72b60933ee2771278f1e225e4a022def55c3c03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893227"
---
# <span data-ttu-id="c50b2-101">Get-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="c50b2-101">Get-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="c50b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c50b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c50b2-103">Listar contratos de marketplace de confluência na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c50b2-103">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="c50b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c50b2-104">SYNTAX</span></span>

```
Get-AzConfluentMarketplaceAgreement [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c50b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c50b2-105">DESCRIPTION</span></span>
<span data-ttu-id="c50b2-106">Listar contratos de marketplace de confluência na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c50b2-106">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="c50b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c50b2-107">EXAMPLES</span></span>

### <span data-ttu-id="c50b2-108">Exemplo 1: Listar todos os contratos de marketplace confluentes em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c50b2-108">Example 1: List all confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentMarketplaceAgreement

Name        Type
----        ----
marketplace Microsoft.Confluent/agreements
confluent   Microsoft.Confluent/offertypes
```

<span data-ttu-id="c50b2-109">Este comando lista todos os contratos de marketplace confluentes em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="c50b2-109">This command lists all confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="c50b2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c50b2-110">PARAMETERS</span></span>

### <span data-ttu-id="c50b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50b2-111">-DefaultProfile</span></span>
<span data-ttu-id="c50b2-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c50b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c50b2-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c50b2-113">-SubscriptionId</span></span>
<span data-ttu-id="c50b2-114">ID de assinatura do Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="c50b2-114">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="c50b2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50b2-115">CommonParameters</span></span>
<span data-ttu-id="c50b2-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c50b2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50b2-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c50b2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50b2-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c50b2-118">INPUTS</span></span>

## <span data-ttu-id="c50b2-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c50b2-119">OUTPUTS</span></span>

### <span data-ttu-id="c50b2-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="c50b2-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="c50b2-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="c50b2-121">NOTES</span></span>

<span data-ttu-id="c50b2-122">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c50b2-122">ALIASES</span></span>

## <span data-ttu-id="c50b2-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c50b2-123">RELATED LINKS</span></span>

