---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 78a9623e5e65c93d302b356b64b5c30033697fdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892110"
---
# <span data-ttu-id="773a4-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="773a4-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="773a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="773a4-102">SYNOPSIS</span></span>
<span data-ttu-id="773a4-103">Obtém a Configuração de Escala Automática do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="773a4-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="773a4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="773a4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="773a4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="773a4-105">DESCRIPTION</span></span>
<span data-ttu-id="773a4-106">O cmdlet **Get-AzApplicationGatewayAutoscaleConfiguration obtém** Configuração de Escala Automática do Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="773a4-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="773a4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="773a4-107">EXAMPLES</span></span>

### <span data-ttu-id="773a4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="773a4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="773a4-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="773a4-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="773a4-110">O segundo comando extrai a configuração de escala automática do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="773a4-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="773a4-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="773a4-111">PARAMETERS</span></span>

### <span data-ttu-id="773a4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="773a4-112">-ApplicationGateway</span></span>
<span data-ttu-id="773a4-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="773a4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="773a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773a4-114">-DefaultProfile</span></span>
<span data-ttu-id="773a4-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="773a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="773a4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773a4-116">CommonParameters</span></span>
<span data-ttu-id="773a4-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="773a4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773a4-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="773a4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773a4-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="773a4-119">INPUTS</span></span>

### <span data-ttu-id="773a4-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="773a4-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="773a4-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="773a4-121">OUTPUTS</span></span>

### <span data-ttu-id="773a4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="773a4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="773a4-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="773a4-123">NOTES</span></span>

## <span data-ttu-id="773a4-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="773a4-124">RELATED LINKS</span></span>

[<span data-ttu-id="773a4-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="773a4-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="773a4-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="773a4-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="773a4-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="773a4-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
