---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 5926b2fb4b97d42ff8743ad227fdfb1b32326a20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887382"
---
# <span data-ttu-id="556db-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="556db-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="556db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="556db-102">SYNOPSIS</span></span>
<span data-ttu-id="556db-103">Adiciona uma porta front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="556db-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="556db-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="556db-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="556db-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="556db-105">DESCRIPTION</span></span>
<span data-ttu-id="556db-106">O cmdlet **Add-AzApplicationGatewayFrontendPort** adiciona uma porta front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="556db-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="556db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="556db-107">EXAMPLES</span></span>

### <span data-ttu-id="556db-108">Exemplo 1: Adicionar uma porta front-end a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="556db-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="556db-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="556db-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="556db-110">O segundo comando adiciona a porta 80 como uma porta front-end para o gateway de aplicativo armazenado em $AppGw e nomeia a porta FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="556db-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="556db-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="556db-111">PARAMETERS</span></span>

### <span data-ttu-id="556db-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="556db-112">-ApplicationGateway</span></span>
<span data-ttu-id="556db-113">Especifica o gateway de aplicativo ao qual este cmdlet adiciona uma porta front-end.</span><span class="sxs-lookup"><span data-stu-id="556db-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="556db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556db-114">-DefaultProfile</span></span>
<span data-ttu-id="556db-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="556db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="556db-116">-Name</span><span class="sxs-lookup"><span data-stu-id="556db-116">-Name</span></span>
<span data-ttu-id="556db-117">Especifica o nome da porta front-end.</span><span class="sxs-lookup"><span data-stu-id="556db-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="556db-118">-Port</span><span class="sxs-lookup"><span data-stu-id="556db-118">-Port</span></span>
<span data-ttu-id="556db-119">Especifica o número da porta.</span><span class="sxs-lookup"><span data-stu-id="556db-119">Specifies the port number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556db-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556db-120">CommonParameters</span></span>
<span data-ttu-id="556db-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="556db-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556db-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="556db-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556db-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="556db-123">INPUTS</span></span>

### <span data-ttu-id="556db-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="556db-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="556db-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="556db-125">OUTPUTS</span></span>

### <span data-ttu-id="556db-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="556db-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="556db-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="556db-127">NOTES</span></span>

## <span data-ttu-id="556db-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="556db-128">RELATED LINKS</span></span>

[<span data-ttu-id="556db-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="556db-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="556db-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="556db-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="556db-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="556db-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="556db-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="556db-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


