---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableWafRuleSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: f8f8411a40ddbc4d0e2f0e4b508385717e0c4173
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775602"
---
# <span data-ttu-id="65bae-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="65bae-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="65bae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65bae-102">SYNOPSIS</span></span>
<span data-ttu-id="65bae-103">Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="65bae-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="65bae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65bae-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65bae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65bae-105">DESCRIPTION</span></span>
<span data-ttu-id="65bae-106">O cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="65bae-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="65bae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65bae-107">EXAMPLES</span></span>

### <span data-ttu-id="65bae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65bae-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="65bae-109">Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="65bae-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="65bae-110">OS</span><span class="sxs-lookup"><span data-stu-id="65bae-110">PARAMETERS</span></span>

### <span data-ttu-id="65bae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65bae-111">-DefaultProfile</span></span>
<span data-ttu-id="65bae-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65bae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65bae-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bae-113">CommonParameters</span></span>
<span data-ttu-id="65bae-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65bae-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bae-115">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65bae-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bae-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65bae-116">INPUTS</span></span>

### <span data-ttu-id="65bae-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="65bae-117">None</span></span>

## <span data-ttu-id="65bae-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65bae-118">OUTPUTS</span></span>

### <span data-ttu-id="65bae-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="65bae-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="65bae-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65bae-120">NOTES</span></span>
<span data-ttu-id="65bae-121">**List-AzApplicationGatewayAvailableWafRuleSet** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="65bae-121">**List-AzApplicationGatewayAvailableWafRuleSet** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="65bae-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65bae-122">RELATED LINKS</span></span>
