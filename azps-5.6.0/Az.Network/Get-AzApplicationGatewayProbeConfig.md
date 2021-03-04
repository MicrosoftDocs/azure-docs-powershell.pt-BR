---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 1bdee7a9ffb35085f8194d86dc9a9486f5dd7fb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890821"
---
# <span data-ttu-id="489d7-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="489d7-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="489d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="489d7-102">SYNOPSIS</span></span>
<span data-ttu-id="489d7-103">Obtém uma configuração de sonda de saúde existente de um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="489d7-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="489d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="489d7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="489d7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="489d7-105">DESCRIPTION</span></span>
<span data-ttu-id="489d7-106">O Get-AzApplicationGatewayProbeConfig cmdlet obtém uma configuração de sonda de saúde existente de um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="489d7-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="489d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="489d7-107">EXAMPLES</span></span>

### <span data-ttu-id="489d7-108">Exemplo 1: Obter uma sonda existente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="489d7-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="489d7-109">Este comando obtém a sonda de saúde chamada Probe02 do gateway de aplicativo chamado Gateway.</span><span class="sxs-lookup"><span data-stu-id="489d7-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="489d7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="489d7-110">PARAMETERS</span></span>

### <span data-ttu-id="489d7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="489d7-111">-ApplicationGateway</span></span>
<span data-ttu-id="489d7-112">Especifica o gateway de aplicativo para o qual este cmdlet obtém uma configuração de sonda.</span><span class="sxs-lookup"><span data-stu-id="489d7-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="489d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="489d7-113">-DefaultProfile</span></span>
<span data-ttu-id="489d7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="489d7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="489d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="489d7-115">-Name</span></span>
<span data-ttu-id="489d7-116">Especifica o nome da sonda.</span><span class="sxs-lookup"><span data-stu-id="489d7-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="489d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489d7-117">CommonParameters</span></span>
<span data-ttu-id="489d7-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="489d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489d7-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="489d7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489d7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="489d7-120">INPUTS</span></span>

### <span data-ttu-id="489d7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="489d7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="489d7-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="489d7-122">OUTPUTS</span></span>

### <span data-ttu-id="489d7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="489d7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="489d7-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="489d7-124">NOTES</span></span>

## <span data-ttu-id="489d7-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="489d7-125">RELATED LINKS</span></span>

[<span data-ttu-id="489d7-126">Adicionar uma sonda a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="489d7-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="489d7-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="489d7-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="489d7-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="489d7-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="489d7-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="489d7-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="489d7-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="489d7-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

