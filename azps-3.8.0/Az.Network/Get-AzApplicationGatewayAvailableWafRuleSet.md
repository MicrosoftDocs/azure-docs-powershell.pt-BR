---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943582"
---
# <span data-ttu-id="c142c-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="c142c-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="c142c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c142c-102">SYNOPSIS</span></span>
<span data-ttu-id="c142c-103">Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c142c-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="c142c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c142c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c142c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c142c-105">DESCRIPTION</span></span>
<span data-ttu-id="c142c-106">O cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c142c-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="c142c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c142c-107">EXAMPLES</span></span>

### <span data-ttu-id="c142c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c142c-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="c142c-109">Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c142c-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="c142c-110">OS</span><span class="sxs-lookup"><span data-stu-id="c142c-110">PARAMETERS</span></span>

### <span data-ttu-id="c142c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c142c-111">-DefaultProfile</span></span>
<span data-ttu-id="c142c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c142c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c142c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c142c-113">CommonParameters</span></span>
<span data-ttu-id="c142c-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c142c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c142c-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c142c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c142c-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c142c-116">INPUTS</span></span>

### <span data-ttu-id="c142c-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c142c-117">None</span></span>

## <span data-ttu-id="c142c-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c142c-118">OUTPUTS</span></span>

### <span data-ttu-id="c142c-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="c142c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="c142c-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c142c-120">NOTES</span></span>
<span data-ttu-id="c142c-121">**List-AzApplicationGatewayAvailableWafRuleSets** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="c142c-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="c142c-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c142c-122">RELATED LINKS</span></span>
