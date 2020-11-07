---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785730"
---
# <span data-ttu-id="0150a-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="0150a-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="0150a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0150a-102">SYNOPSIS</span></span>
<span data-ttu-id="0150a-103">Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0150a-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0150a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0150a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0150a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0150a-105">DESCRIPTION</span></span>
<span data-ttu-id="0150a-106">O cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0150a-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="0150a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0150a-107">EXAMPLES</span></span>

### <span data-ttu-id="0150a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0150a-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="0150a-109">Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0150a-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="0150a-110">OS</span><span class="sxs-lookup"><span data-stu-id="0150a-110">PARAMETERS</span></span>

### <span data-ttu-id="0150a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0150a-111">-DefaultProfile</span></span>
<span data-ttu-id="0150a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0150a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0150a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0150a-113">CommonParameters</span></span>
<span data-ttu-id="0150a-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0150a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0150a-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0150a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0150a-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0150a-116">INPUTS</span></span>

### <span data-ttu-id="0150a-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0150a-117">None</span></span>

## <span data-ttu-id="0150a-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0150a-118">OUTPUTS</span></span>

### <span data-ttu-id="0150a-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="0150a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="0150a-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0150a-120">NOTES</span></span>
<span data-ttu-id="0150a-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** é um alias para o cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="0150a-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="0150a-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0150a-122">RELATED LINKS</span></span>

