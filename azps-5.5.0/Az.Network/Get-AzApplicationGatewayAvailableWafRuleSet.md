---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114185"
---
# <span data-ttu-id="1940a-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="1940a-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="1940a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1940a-102">SYNOPSIS</span></span>
<span data-ttu-id="1940a-103">Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1940a-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="1940a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1940a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1940a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1940a-105">DESCRIPTION</span></span>
<span data-ttu-id="1940a-106">O **cmdlet Get-AzApplicationGatewayAvailableWafRuleSet** obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1940a-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="1940a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1940a-107">EXAMPLES</span></span>

### <span data-ttu-id="1940a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1940a-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="1940a-109">Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1940a-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="1940a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1940a-110">PARAMETERS</span></span>

### <span data-ttu-id="1940a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1940a-111">-DefaultProfile</span></span>
<span data-ttu-id="1940a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1940a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1940a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1940a-113">CommonParameters</span></span>
<span data-ttu-id="1940a-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1940a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1940a-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1940a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1940a-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="1940a-116">INPUTS</span></span>

### <span data-ttu-id="1940a-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1940a-117">None</span></span>

## <span data-ttu-id="1940a-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="1940a-118">OUTPUTS</span></span>

### <span data-ttu-id="1940a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="1940a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="1940a-120">Notas</span><span class="sxs-lookup"><span data-stu-id="1940a-120">NOTES</span></span>
<span data-ttu-id="1940a-121">**List-AzApplicationGatewayAvailableWafRuleSets** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="1940a-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="1940a-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1940a-122">RELATED LINKS</span></span>
