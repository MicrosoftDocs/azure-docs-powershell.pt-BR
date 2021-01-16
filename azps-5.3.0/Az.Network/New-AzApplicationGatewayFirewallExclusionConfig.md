---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271791"
---
# <span data-ttu-id="45ed2-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="45ed2-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="45ed2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="45ed2-103">Cria uma nova lista de regras de exclusão para o Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="45ed2-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="45ed2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45ed2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45ed2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45ed2-105">DESCRIPTION</span></span>
<span data-ttu-id="45ed2-106">O cmdlet **New-AzApplicationGatewayFirewallExclusionConfig** uma nova lista de regras de exclusão para aplicativos do gateway de WAF.</span><span class="sxs-lookup"><span data-stu-id="45ed2-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="45ed2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45ed2-107">EXAMPLES</span></span>

### <span data-ttu-id="45ed2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45ed2-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="45ed2-109">Esse comando cria uma nova configuração de listas de regras de exclusão para a variável chamada RequestHeaderNames e o operador chamado StartsWith e selector chamado XYZ.</span><span class="sxs-lookup"><span data-stu-id="45ed2-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="45ed2-110">A configuração da lista de exclusão é salva no $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="45ed2-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="45ed2-111">OS</span><span class="sxs-lookup"><span data-stu-id="45ed2-111">PARAMETERS</span></span>

### <span data-ttu-id="45ed2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ed2-112">-DefaultProfile</span></span>
<span data-ttu-id="45ed2-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45ed2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ed2-114">-Operador</span><span class="sxs-lookup"><span data-stu-id="45ed2-114">-Operator</span></span>
<span data-ttu-id="45ed2-115">Quando variável é uma coleção, opere no seletor para especificar a quais elementos da coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="45ed2-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ed2-116">-Seletor</span><span class="sxs-lookup"><span data-stu-id="45ed2-116">-Selector</span></span>
<span data-ttu-id="45ed2-117">Quando Variable é uma coleção, operador usado para especificar a quais elementos da coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="45ed2-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ed2-118">-Variável</span><span class="sxs-lookup"><span data-stu-id="45ed2-118">-Variable</span></span>
<span data-ttu-id="45ed2-119">A variável a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="45ed2-119">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ed2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ed2-120">CommonParameters</span></span>
<span data-ttu-id="45ed2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ed2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ed2-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ed2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ed2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45ed2-123">INPUTS</span></span>

### <span data-ttu-id="45ed2-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="45ed2-124">None</span></span>

## <span data-ttu-id="45ed2-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45ed2-125">OUTPUTS</span></span>

### <span data-ttu-id="45ed2-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="45ed2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="45ed2-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45ed2-127">NOTES</span></span>

## <span data-ttu-id="45ed2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45ed2-128">RELATED LINKS</span></span>
