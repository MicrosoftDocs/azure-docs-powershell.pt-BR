---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: b914e87729e97bb6b8af9ec59605290e0cc025bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888681"
---
# <span data-ttu-id="19da7-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="19da7-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="19da7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19da7-102">SYNOPSIS</span></span>
<span data-ttu-id="19da7-103">Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="19da7-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="19da7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="19da7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19da7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="19da7-105">DESCRIPTION</span></span>
<span data-ttu-id="19da7-106">O cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="19da7-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="19da7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19da7-107">EXAMPLES</span></span>

### <span data-ttu-id="19da7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="19da7-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="19da7-109">Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="19da7-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="19da7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="19da7-110">PARAMETERS</span></span>

### <span data-ttu-id="19da7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19da7-111">-DefaultProfile</span></span>
<span data-ttu-id="19da7-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="19da7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19da7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19da7-113">CommonParameters</span></span>
<span data-ttu-id="19da7-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19da7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19da7-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19da7-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19da7-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19da7-116">INPUTS</span></span>

### <span data-ttu-id="19da7-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="19da7-117">None</span></span>

## <span data-ttu-id="19da7-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="19da7-118">OUTPUTS</span></span>

### <span data-ttu-id="19da7-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="19da7-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="19da7-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="19da7-120">NOTES</span></span>
<span data-ttu-id="19da7-121">**List-AzApplicationGatewayAvailableWafRuleSets** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="19da7-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="19da7-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19da7-122">RELATED LINKS</span></span>
