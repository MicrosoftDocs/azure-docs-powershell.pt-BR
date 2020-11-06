---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: fb16474d8a23f528aaaeb498ced4fa5a3e952236
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441590"
---
# <span data-ttu-id="fc8a6-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="fc8a6-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="fc8a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8a6-103">Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc8a6-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc8a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc8a6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc8a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="fc8a6-106">O cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc8a6-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="fc8a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc8a6-107">EXAMPLES</span></span>

### <span data-ttu-id="fc8a6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc8a6-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="fc8a6-109">Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc8a6-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="fc8a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="fc8a6-110">PARAMETERS</span></span>

### <span data-ttu-id="fc8a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8a6-111">-DefaultProfile</span></span>
<span data-ttu-id="fc8a6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc8a6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8a6-113">CommonParameters</span></span>
<span data-ttu-id="fc8a6-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8a6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8a6-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8a6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8a6-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc8a6-116">INPUTS</span></span>

### <span data-ttu-id="fc8a6-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fc8a6-117">None</span></span>

## <span data-ttu-id="fc8a6-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc8a6-118">OUTPUTS</span></span>

### <span data-ttu-id="fc8a6-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="fc8a6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="fc8a6-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc8a6-120">NOTES</span></span>
<span data-ttu-id="fc8a6-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** é um alias para o cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="fc8a6-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="fc8a6-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc8a6-122">RELATED LINKS</span></span>
