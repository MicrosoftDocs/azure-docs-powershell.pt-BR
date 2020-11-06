---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: 9dcb9720c194fbad4e82607f50132c9bbc5415c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597590"
---
# <span data-ttu-id="302f4-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="302f4-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="302f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="302f4-102">SYNOPSIS</span></span>
<span data-ttu-id="302f4-103">Cria uma política de entrega.</span><span class="sxs-lookup"><span data-stu-id="302f4-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="302f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="302f4-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="302f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="302f4-105">DESCRIPTION</span></span>
<span data-ttu-id="302f4-106">O cmdlet **New-AzCdnDeliveryPolicy** cria uma política de entrega para criação de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="302f4-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="302f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="302f4-107">EXAMPLES</span></span>

### <span data-ttu-id="302f4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="302f4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="302f4-109">Criar uma política de entrega de exemplo</span><span class="sxs-lookup"><span data-stu-id="302f4-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="302f4-110">OS</span><span class="sxs-lookup"><span data-stu-id="302f4-110">PARAMETERS</span></span>

### <span data-ttu-id="302f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302f4-111">-DefaultProfile</span></span>
<span data-ttu-id="302f4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="302f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302f4-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="302f4-113">-Description</span></span>
<span data-ttu-id="302f4-114">Descrição da política</span><span class="sxs-lookup"><span data-stu-id="302f4-114">Description of the policy</span></span>

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

### <span data-ttu-id="302f4-115">-Regra</span><span class="sxs-lookup"><span data-stu-id="302f4-115">-Rule</span></span>
<span data-ttu-id="302f4-116">Uma lista de deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="302f4-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="302f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302f4-117">CommonParameters</span></span>
<span data-ttu-id="302f4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302f4-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="302f4-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302f4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="302f4-120">INPUTS</span></span>

### <span data-ttu-id="302f4-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="302f4-121">None</span></span>

## <span data-ttu-id="302f4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="302f4-122">OUTPUTS</span></span>

### <span data-ttu-id="302f4-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="302f4-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="302f4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="302f4-124">NOTES</span></span>

## <span data-ttu-id="302f4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="302f4-125">RELATED LINKS</span></span>
