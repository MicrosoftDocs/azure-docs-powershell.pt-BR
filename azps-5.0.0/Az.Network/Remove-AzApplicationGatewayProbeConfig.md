---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115970"
---
# <span data-ttu-id="34d3d-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="34d3d-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="34d3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="34d3d-103">Remove uma investigação de integridade de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="34d3d-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="34d3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34d3d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34d3d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34d3d-105">DESCRIPTION</span></span>
<span data-ttu-id="34d3d-106">O cmdlet Remove-AzApplicationGatewayProbeConfig remove um teste Heath de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="34d3d-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="34d3d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34d3d-107">EXAMPLES</span></span>

### <span data-ttu-id="34d3d-108">Exemplo 1: remover um teste de integridade de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="34d3d-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="34d3d-109">Esse comando Remove o teste de integridade chamado Probe04 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="34d3d-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="34d3d-110">OS</span><span class="sxs-lookup"><span data-stu-id="34d3d-110">PARAMETERS</span></span>

### <span data-ttu-id="34d3d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34d3d-111">-ApplicationGateway</span></span>
<span data-ttu-id="34d3d-112">Especifica o gateway do aplicativo para o qual esse cmdlet Remove um teste.</span><span class="sxs-lookup"><span data-stu-id="34d3d-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="34d3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d3d-113">-DefaultProfile</span></span>
<span data-ttu-id="34d3d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34d3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34d3d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="34d3d-115">-Name</span></span>
<span data-ttu-id="34d3d-116">Especifica o nome do teste para o qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="34d3d-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="34d3d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d3d-117">CommonParameters</span></span>
<span data-ttu-id="34d3d-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d3d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d3d-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d3d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d3d-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34d3d-120">INPUTS</span></span>

### <span data-ttu-id="34d3d-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34d3d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34d3d-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34d3d-122">OUTPUTS</span></span>

### <span data-ttu-id="34d3d-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34d3d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34d3d-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34d3d-124">NOTES</span></span>

## <span data-ttu-id="34d3d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34d3d-125">RELATED LINKS</span></span>

[<span data-ttu-id="34d3d-126">Remover um teste de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="34d3d-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="34d3d-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="34d3d-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="34d3d-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="34d3d-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="34d3d-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="34d3d-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="34d3d-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="34d3d-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

