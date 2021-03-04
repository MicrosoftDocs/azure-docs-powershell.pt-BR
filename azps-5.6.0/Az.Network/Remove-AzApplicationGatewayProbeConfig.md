---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 8ee58ee3f6c7a92fac0cb3c92f0a45966e4e875e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890381"
---
# <span data-ttu-id="e2fb7-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2fb7-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e2fb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fb7-103">Remove uma sonda de saúde de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="e2fb7-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="e2fb7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e2fb7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2fb7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e2fb7-105">DESCRIPTION</span></span>
<span data-ttu-id="e2fb7-106">O Remove-AzApplicationGatewayProbeConfig cmdlet remove uma sonda de saúde de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="e2fb7-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="e2fb7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2fb7-107">EXAMPLES</span></span>

### <span data-ttu-id="e2fb7-108">Exemplo 1: Remover uma sonda de saúde de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="e2fb7-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="e2fb7-109">Este comando remove a sonda de saúde chamada Probe04 do gateway de aplicativo chamado Gateway.</span><span class="sxs-lookup"><span data-stu-id="e2fb7-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="e2fb7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e2fb7-110">PARAMETERS</span></span>

### <span data-ttu-id="e2fb7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2fb7-111">-ApplicationGateway</span></span>
<span data-ttu-id="e2fb7-112">Especifica o gateway de aplicativo para o qual este cmdlet remove uma sonda.</span><span class="sxs-lookup"><span data-stu-id="e2fb7-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="e2fb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fb7-113">-DefaultProfile</span></span>
<span data-ttu-id="e2fb7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e2fb7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2fb7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e2fb7-115">-Name</span></span>
<span data-ttu-id="e2fb7-116">Especifica o nome da sonda para a qual este cmdlet é removido.</span><span class="sxs-lookup"><span data-stu-id="e2fb7-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fb7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fb7-117">CommonParameters</span></span>
<span data-ttu-id="e2fb7-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2fb7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fb7-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2fb7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fb7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2fb7-120">INPUTS</span></span>

### <span data-ttu-id="e2fb7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2fb7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2fb7-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e2fb7-122">OUTPUTS</span></span>

### <span data-ttu-id="e2fb7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2fb7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2fb7-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="e2fb7-124">NOTES</span></span>

## <span data-ttu-id="e2fb7-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2fb7-125">RELATED LINKS</span></span>

[<span data-ttu-id="e2fb7-126">Remover uma sonda de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="e2fb7-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="e2fb7-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2fb7-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e2fb7-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2fb7-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e2fb7-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2fb7-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="e2fb7-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e2fb7-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

