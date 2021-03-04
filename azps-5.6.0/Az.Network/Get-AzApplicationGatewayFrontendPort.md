---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: a0e8cbdb9ec64d4f65b859f70c1a1bb7f843132b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891171"
---
# <span data-ttu-id="cb95d-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb95d-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="cb95d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb95d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb95d-103">Obtém a porta front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb95d-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="cb95d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cb95d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb95d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cb95d-105">DESCRIPTION</span></span>
<span data-ttu-id="cb95d-106">O cmdlet **Get-AzApplicationGatewayFrontendPort** obtém a porta front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cb95d-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="cb95d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb95d-107">EXAMPLES</span></span>

### <span data-ttu-id="cb95d-108">Exemplo 1: Obter uma porta front-end especificada</span><span class="sxs-lookup"><span data-stu-id="cb95d-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="cb95d-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cb95d-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cb95d-110">O segundo comando obtém a porta front-end chamada FrontEndPort01 $AppGw e a armazena na variável $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="cb95d-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="cb95d-111">Exemplo 2: Obter uma lista de portas front-end</span><span class="sxs-lookup"><span data-stu-id="cb95d-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="cb95d-112">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cb95d-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cb95d-113">O segundo comando obtém uma lista das portas front-end $AppGw e as armazena na variável $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="cb95d-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="cb95d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cb95d-114">PARAMETERS</span></span>

### <span data-ttu-id="cb95d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb95d-115">-ApplicationGateway</span></span>
<span data-ttu-id="cb95d-116">Especifica o objeto gateway de aplicativo que contém a porta front-end.</span><span class="sxs-lookup"><span data-stu-id="cb95d-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="cb95d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb95d-117">-DefaultProfile</span></span>
<span data-ttu-id="cb95d-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cb95d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb95d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cb95d-119">-Name</span></span>
<span data-ttu-id="cb95d-120">Especifica o nome da porta front-end a ser obter.</span><span class="sxs-lookup"><span data-stu-id="cb95d-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="cb95d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb95d-121">CommonParameters</span></span>
<span data-ttu-id="cb95d-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb95d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb95d-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb95d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb95d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb95d-124">INPUTS</span></span>

### <span data-ttu-id="cb95d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb95d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb95d-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cb95d-126">OUTPUTS</span></span>

### <span data-ttu-id="cb95d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb95d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="cb95d-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="cb95d-128">NOTES</span></span>

## <span data-ttu-id="cb95d-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb95d-129">RELATED LINKS</span></span>

[<span data-ttu-id="cb95d-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb95d-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cb95d-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb95d-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cb95d-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb95d-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cb95d-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb95d-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


