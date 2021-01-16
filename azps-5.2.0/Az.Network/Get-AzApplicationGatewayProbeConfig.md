---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257228"
---
# <span data-ttu-id="db09f-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="db09f-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="db09f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db09f-102">SYNOPSIS</span></span>
<span data-ttu-id="db09f-103">Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="db09f-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="db09f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db09f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db09f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db09f-105">DESCRIPTION</span></span>
<span data-ttu-id="db09f-106">O cmdlet Get-AzApplicationGatewayProbeConfig Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="db09f-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="db09f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db09f-107">EXAMPLES</span></span>

### <span data-ttu-id="db09f-108">Exemplo 1: obter um teste existente de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="db09f-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="db09f-109">Esse comando obtém o teste de integridade chamado Probe02 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="db09f-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="db09f-110">OS</span><span class="sxs-lookup"><span data-stu-id="db09f-110">PARAMETERS</span></span>

### <span data-ttu-id="db09f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db09f-111">-ApplicationGateway</span></span>
<span data-ttu-id="db09f-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="db09f-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="db09f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db09f-113">-DefaultProfile</span></span>
<span data-ttu-id="db09f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db09f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db09f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="db09f-115">-Name</span></span>
<span data-ttu-id="db09f-116">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="db09f-116">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db09f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db09f-117">CommonParameters</span></span>
<span data-ttu-id="db09f-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db09f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db09f-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db09f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db09f-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db09f-120">INPUTS</span></span>

### <span data-ttu-id="db09f-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db09f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="db09f-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db09f-122">OUTPUTS</span></span>

### <span data-ttu-id="db09f-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="db09f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="db09f-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db09f-124">NOTES</span></span>

## <span data-ttu-id="db09f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db09f-125">RELATED LINKS</span></span>

[<span data-ttu-id="db09f-126">Adicionar um teste a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="db09f-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="db09f-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="db09f-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="db09f-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="db09f-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="db09f-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="db09f-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="db09f-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="db09f-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

