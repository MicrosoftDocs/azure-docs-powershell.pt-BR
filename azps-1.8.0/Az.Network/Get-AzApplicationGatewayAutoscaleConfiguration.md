---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 723d1aaab342673f16d37cfaa15406f3ab99566d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600675"
---
# <span data-ttu-id="914ca-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="914ca-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="914ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="914ca-102">SYNOPSIS</span></span>
<span data-ttu-id="914ca-103">Obtém a configuração de autoescala do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="914ca-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="914ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="914ca-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="914ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="914ca-105">DESCRIPTION</span></span>
<span data-ttu-id="914ca-106">O cmdlet **Get-AzApplicationGatewayAutoscaleConfiguration** Obtém a configuração de autoescala do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="914ca-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="914ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="914ca-107">EXAMPLES</span></span>

### <span data-ttu-id="914ca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="914ca-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="914ca-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="914ca-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="914ca-110">O segundo comando extrai a configuração de autoescala do gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="914ca-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="914ca-111">OS</span><span class="sxs-lookup"><span data-stu-id="914ca-111">PARAMETERS</span></span>

### <span data-ttu-id="914ca-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="914ca-112">-ApplicationGateway</span></span>
<span data-ttu-id="914ca-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="914ca-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="914ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="914ca-114">-DefaultProfile</span></span>
<span data-ttu-id="914ca-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="914ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="914ca-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="914ca-116">CommonParameters</span></span>
<span data-ttu-id="914ca-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="914ca-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="914ca-118">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="914ca-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="914ca-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="914ca-119">INPUTS</span></span>

### <span data-ttu-id="914ca-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="914ca-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="914ca-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="914ca-121">OUTPUTS</span></span>

### <span data-ttu-id="914ca-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="914ca-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="914ca-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="914ca-123">NOTES</span></span>

## <span data-ttu-id="914ca-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="914ca-124">RELATED LINKS</span></span>

[<span data-ttu-id="914ca-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="914ca-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="914ca-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="914ca-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="914ca-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="914ca-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
