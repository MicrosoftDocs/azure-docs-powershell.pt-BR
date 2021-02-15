---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111662"
---
# <span data-ttu-id="268fc-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="268fc-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="268fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="268fc-102">SYNOPSIS</span></span>
<span data-ttu-id="268fc-103">Cria uma nova lista de regras de exclusão para waf do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="268fc-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="268fc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="268fc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268fc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="268fc-105">DESCRIPTION</span></span>
<span data-ttu-id="268fc-106">O **cmdlet New-AzApplicationGatewayFirewallExclusionConfig** uma nova lista de regras de exclusão para waf do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="268fc-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="268fc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="268fc-107">EXAMPLES</span></span>

### <span data-ttu-id="268fc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="268fc-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="268fc-109">Esse comando cria uma nova configuração de listas de regras de exclusão para a variável nomeada NomeDoSuárioDoSuletor e operador chamado StartsWith e Seletor denominado xyz.</span><span class="sxs-lookup"><span data-stu-id="268fc-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="268fc-110">A configuração da lista de exclusão é salva $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="268fc-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="268fc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="268fc-111">PARAMETERS</span></span>

### <span data-ttu-id="268fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268fc-112">-DefaultProfile</span></span>
<span data-ttu-id="268fc-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="268fc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="268fc-114">-Operador</span><span class="sxs-lookup"><span data-stu-id="268fc-114">-Operator</span></span>
<span data-ttu-id="268fc-115">Quando variável for uma coleção, operar no seletor para especificar a quais elementos da coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="268fc-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="268fc-116">-Seletor</span><span class="sxs-lookup"><span data-stu-id="268fc-116">-Selector</span></span>
<span data-ttu-id="268fc-117">Quando variável é uma coleção, o operador usado para especificar a quais elementos na coleção essa exclusão se aplica.</span><span class="sxs-lookup"><span data-stu-id="268fc-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="268fc-118">-Variável</span><span class="sxs-lookup"><span data-stu-id="268fc-118">-Variable</span></span>
<span data-ttu-id="268fc-119">A variável a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="268fc-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="268fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268fc-120">CommonParameters</span></span>
<span data-ttu-id="268fc-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268fc-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268fc-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268fc-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="268fc-123">INPUTS</span></span>

### <span data-ttu-id="268fc-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="268fc-124">None</span></span>

## <span data-ttu-id="268fc-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="268fc-125">OUTPUTS</span></span>

### <span data-ttu-id="268fc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="268fc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="268fc-127">Notas</span><span class="sxs-lookup"><span data-stu-id="268fc-127">NOTES</span></span>

## <span data-ttu-id="268fc-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="268fc-128">RELATED LINKS</span></span>
