---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: e550d00d1d952fb372db81ec87a35c701d6dedde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771812"
---
# <span data-ttu-id="cd257-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd257-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="cd257-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd257-102">SYNOPSIS</span></span>
<span data-ttu-id="cd257-103">Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cd257-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="cd257-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd257-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd257-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd257-105">DESCRIPTION</span></span>
<span data-ttu-id="cd257-106">O cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cd257-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="cd257-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd257-107">EXAMPLES</span></span>

### <span data-ttu-id="cd257-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd257-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="cd257-109">Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cd257-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="cd257-110">OS</span><span class="sxs-lookup"><span data-stu-id="cd257-110">PARAMETERS</span></span>

### <span data-ttu-id="cd257-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd257-111">-DefaultProfile</span></span>
<span data-ttu-id="cd257-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd257-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd257-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd257-113">CommonParameters</span></span>
<span data-ttu-id="cd257-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd257-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd257-115">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd257-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd257-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd257-116">INPUTS</span></span>

### <span data-ttu-id="cd257-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cd257-117">None</span></span>

## <span data-ttu-id="cd257-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd257-118">OUTPUTS</span></span>

### <span data-ttu-id="cd257-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="cd257-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="cd257-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd257-120">NOTES</span></span>
<span data-ttu-id="cd257-121">**List-AzApplicationGatewayAvailableWafRuleSets** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="cd257-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="cd257-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd257-122">RELATED LINKS</span></span>