---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117360"
---
# <span data-ttu-id="2904a-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2904a-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2904a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2904a-102">SYNOPSIS</span></span>
<span data-ttu-id="2904a-103">Remove um problema de saúde de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="2904a-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="2904a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2904a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2904a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2904a-105">DESCRIPTION</span></span>
<span data-ttu-id="2904a-106">O Remove-AzApplicationGatewayProbeConfig cmdlet remove um problema de saúde de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="2904a-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="2904a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2904a-107">EXAMPLES</span></span>

### <span data-ttu-id="2904a-108">Exemplo 1: Remover um problema de saúde de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="2904a-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="2904a-109">Esse comando remove a confirmação de saúde chamada " Nome04 " do gateway de aplicativo chamado Gateway.</span><span class="sxs-lookup"><span data-stu-id="2904a-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="2904a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2904a-110">PARAMETERS</span></span>

### <span data-ttu-id="2904a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2904a-111">-ApplicationGateway</span></span>
<span data-ttu-id="2904a-112">Especifica o gateway do aplicativo para o qual este cmdlet remove uma busca.</span><span class="sxs-lookup"><span data-stu-id="2904a-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="2904a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2904a-113">-DefaultProfile</span></span>
<span data-ttu-id="2904a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2904a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2904a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2904a-115">-Name</span></span>
<span data-ttu-id="2904a-116">Especifica o nome da sonda para a qual este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="2904a-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="2904a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2904a-117">CommonParameters</span></span>
<span data-ttu-id="2904a-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2904a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2904a-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2904a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2904a-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="2904a-120">INPUTS</span></span>

### <span data-ttu-id="2904a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2904a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2904a-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="2904a-122">OUTPUTS</span></span>

### <span data-ttu-id="2904a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2904a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2904a-124">Notas</span><span class="sxs-lookup"><span data-stu-id="2904a-124">NOTES</span></span>

## <span data-ttu-id="2904a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2904a-125">RELATED LINKS</span></span>

[<span data-ttu-id="2904a-126">Remover uma suação de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="2904a-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="2904a-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2904a-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2904a-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2904a-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2904a-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2904a-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="2904a-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2904a-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

