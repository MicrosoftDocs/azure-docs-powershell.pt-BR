---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114193"
---
# <span data-ttu-id="c9bd9-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9bd9-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c9bd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bd9-103">Obtém a Configuração de Escala Automática do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="c9bd9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9bd9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9bd9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9bd9-105">DESCRIPTION</span></span>
<span data-ttu-id="c9bd9-106">O cmdlet **Get-AzApplicationGatewayAutoscaleConfiguration** obtém a Configuração de Escala Automática do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="c9bd9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9bd9-107">EXAMPLES</span></span>

### <span data-ttu-id="c9bd9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9bd9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="c9bd9-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c9bd9-110">O segundo comando extrai a configuração de escala automática do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="c9bd9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9bd9-111">PARAMETERS</span></span>

### <span data-ttu-id="c9bd9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9bd9-112">-ApplicationGateway</span></span>
<span data-ttu-id="c9bd9-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9bd9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c9bd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bd9-114">-DefaultProfile</span></span>
<span data-ttu-id="c9bd9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9bd9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bd9-116">CommonParameters</span></span>
<span data-ttu-id="c9bd9-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9bd9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bd9-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9bd9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bd9-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="c9bd9-119">INPUTS</span></span>

### <span data-ttu-id="c9bd9-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9bd9-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9bd9-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="c9bd9-121">OUTPUTS</span></span>

### <span data-ttu-id="c9bd9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9bd9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c9bd9-123">Notas</span><span class="sxs-lookup"><span data-stu-id="c9bd9-123">NOTES</span></span>

## <span data-ttu-id="c9bd9-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9bd9-124">RELATED LINKS</span></span>

[<span data-ttu-id="c9bd9-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9bd9-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c9bd9-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9bd9-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c9bd9-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9bd9-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
