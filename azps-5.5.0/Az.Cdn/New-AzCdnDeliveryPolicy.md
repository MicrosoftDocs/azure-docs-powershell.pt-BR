---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111187"
---
# <span data-ttu-id="23889-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="23889-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="23889-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23889-102">SYNOPSIS</span></span>
<span data-ttu-id="23889-103">Cria uma política de entrega.</span><span class="sxs-lookup"><span data-stu-id="23889-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="23889-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23889-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23889-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="23889-105">DESCRIPTION</span></span>
<span data-ttu-id="23889-106">O cmdlet **New-AzCdnDeliveryPolicy** cria uma política de entrega para a criação de pontos de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="23889-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="23889-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23889-107">EXAMPLES</span></span>

### <span data-ttu-id="23889-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23889-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="23889-109">Criar uma política de entrega de exemplo</span><span class="sxs-lookup"><span data-stu-id="23889-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="23889-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23889-110">PARAMETERS</span></span>

### <span data-ttu-id="23889-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23889-111">-DefaultProfile</span></span>
<span data-ttu-id="23889-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23889-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23889-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="23889-113">-Description</span></span>
<span data-ttu-id="23889-114">Descrição da política</span><span class="sxs-lookup"><span data-stu-id="23889-114">Description of the policy</span></span>

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

### <span data-ttu-id="23889-115">-Regra</span><span class="sxs-lookup"><span data-stu-id="23889-115">-Rule</span></span>
<span data-ttu-id="23889-116">Uma lista de deliveryRules.</span><span class="sxs-lookup"><span data-stu-id="23889-116">A list of deliveryRules.</span></span>

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

### <span data-ttu-id="23889-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23889-117">CommonParameters</span></span>
<span data-ttu-id="23889-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23889-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23889-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23889-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23889-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="23889-120">INPUTS</span></span>

### <span data-ttu-id="23889-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="23889-121">None</span></span>

## <span data-ttu-id="23889-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="23889-122">OUTPUTS</span></span>

### <span data-ttu-id="23889-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="23889-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="23889-124">Notas</span><span class="sxs-lookup"><span data-stu-id="23889-124">NOTES</span></span>

## <span data-ttu-id="23889-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23889-125">RELATED LINKS</span></span>
