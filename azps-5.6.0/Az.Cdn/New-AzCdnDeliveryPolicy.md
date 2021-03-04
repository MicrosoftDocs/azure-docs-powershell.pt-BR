---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 01cadd267a98cab239b7a83357d308d8dd2d32bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891882"
---
# <span data-ttu-id="a6366-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a6366-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="a6366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6366-102">SYNOPSIS</span></span>
<span data-ttu-id="a6366-103">Cria uma política de entrega.</span><span class="sxs-lookup"><span data-stu-id="a6366-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="a6366-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6366-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6366-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6366-105">DESCRIPTION</span></span>
<span data-ttu-id="a6366-106">O cmdlet **New-AzCdnDeliveryPolicy** cria uma política de entrega para criação de ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="a6366-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="a6366-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6366-107">EXAMPLES</span></span>

### <span data-ttu-id="a6366-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6366-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="a6366-109">Criar uma política de entrega de exemplo</span><span class="sxs-lookup"><span data-stu-id="a6366-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="a6366-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6366-110">PARAMETERS</span></span>

### <span data-ttu-id="a6366-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6366-111">-DefaultProfile</span></span>
<span data-ttu-id="a6366-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6366-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6366-113">-Description</span><span class="sxs-lookup"><span data-stu-id="a6366-113">-Description</span></span>
<span data-ttu-id="a6366-114">Descrição da política</span><span class="sxs-lookup"><span data-stu-id="a6366-114">Description of the policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6366-115">-Rule</span><span class="sxs-lookup"><span data-stu-id="a6366-115">-Rule</span></span>
<span data-ttu-id="a6366-116">Uma lista de deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="a6366-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6366-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6366-117">CommonParameters</span></span>
<span data-ttu-id="a6366-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6366-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6366-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6366-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6366-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6366-120">INPUTS</span></span>

### <span data-ttu-id="a6366-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a6366-121">None</span></span>

## <span data-ttu-id="a6366-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6366-122">OUTPUTS</span></span>

### <span data-ttu-id="a6366-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a6366-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="a6366-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6366-124">NOTES</span></span>

## <span data-ttu-id="a6366-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6366-125">RELATED LINKS</span></span>
