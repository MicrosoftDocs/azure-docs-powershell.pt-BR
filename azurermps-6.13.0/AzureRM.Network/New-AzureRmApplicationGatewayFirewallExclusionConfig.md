---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 570e2df066f9e56b7926bf2d0926c484a0654977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431359"
---
# <span data-ttu-id="85512-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="85512-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="85512-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85512-102">SYNOPSIS</span></span>
<span data-ttu-id="85512-103">Cria uma nova lista de regras de exclusão para o Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="85512-103">Creates a new exclusion rule list for application gateway waf</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85512-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85512-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85512-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85512-105">DESCRIPTION</span></span>
<span data-ttu-id="85512-106">O cmdlet **New-AzureRmApplicationGatewayFirewallExclusionConfig** uma nova lista de regras de exclusão para aplicativos do gateway de WAF.</span><span class="sxs-lookup"><span data-stu-id="85512-106">The **New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="85512-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85512-107">EXAMPLES</span></span>

### <span data-ttu-id="85512-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85512-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="85512-109">Esse comando cria uma nova configuração de listas de regras de exclusão para a variável chamada RequestHeaderNames e o operador chamado StartsWith e selector chamado XYZ.</span><span class="sxs-lookup"><span data-stu-id="85512-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="85512-110">A configuração da lista de exclusão é salva no $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="85512-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="85512-111">OS</span><span class="sxs-lookup"><span data-stu-id="85512-111">PARAMETERS</span></span>

### <span data-ttu-id="85512-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85512-112">-DefaultProfile</span></span>
<span data-ttu-id="85512-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85512-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85512-114">-Operador</span><span class="sxs-lookup"><span data-stu-id="85512-114">-Operator</span></span>
<span data-ttu-id="85512-115">Quando variável é uma coleção, opere no seletor para especificar a quais elementos da coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="85512-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="85512-116">-Seletor</span><span class="sxs-lookup"><span data-stu-id="85512-116">-Selector</span></span>
<span data-ttu-id="85512-117">Quando Variable é uma coleção, operador usado para especificar a quais elementos da coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="85512-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="85512-118">-Variável</span><span class="sxs-lookup"><span data-stu-id="85512-118">-Variable</span></span>
<span data-ttu-id="85512-119">A variável a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="85512-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="85512-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85512-120">CommonParameters</span></span>
<span data-ttu-id="85512-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85512-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85512-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85512-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85512-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85512-123">INPUTS</span></span>

### <span data-ttu-id="85512-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85512-124">None</span></span>

## <span data-ttu-id="85512-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85512-125">OUTPUTS</span></span>

### <span data-ttu-id="85512-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="85512-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="85512-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85512-127">NOTES</span></span>

## <span data-ttu-id="85512-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85512-128">RELATED LINKS</span></span>
