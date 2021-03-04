---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 367d4efc8332b862a8db276934acfa971d7c0d9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891803"
---
# <span data-ttu-id="d6163-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6163-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d6163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6163-102">SYNOPSIS</span></span>
<span data-ttu-id="d6163-103">Obtém a configuração IP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6163-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="d6163-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d6163-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6163-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d6163-105">DESCRIPTION</span></span>
<span data-ttu-id="d6163-106">O cmdlet **Get-AzApplicationGatewayIPConfiguration obtém** a configuração IP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6163-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="d6163-107">A configuração ip contém a sub-rede na qual o gateway de aplicativo é implantado.</span><span class="sxs-lookup"><span data-stu-id="d6163-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="d6163-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6163-108">EXAMPLES</span></span>

### <span data-ttu-id="d6163-109">Exemplo 1: Obter uma configuração IP específica</span><span class="sxs-lookup"><span data-stu-id="d6163-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d6163-110">O primeiro comando obtém um gateway de aplicativo e o armazena na $AppGw variável. O segundo comando obtém uma configuração IP chamada GateSubnet01 do gateway armazenado $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d6163-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="d6163-111">Exemplo 2: obter uma lista de configurações IP</span><span class="sxs-lookup"><span data-stu-id="d6163-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="d6163-112">O primeiro comando obtém um gateway de aplicativo e o armazena na $AppGw variável. O segundo comando obtém uma lista de todas as configurações ip.</span><span class="sxs-lookup"><span data-stu-id="d6163-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="d6163-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d6163-113">PARAMETERS</span></span>

### <span data-ttu-id="d6163-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6163-114">-ApplicationGateway</span></span>
<span data-ttu-id="d6163-115">Especifica o objeto gateway de aplicativo que contém configuração IP.</span><span class="sxs-lookup"><span data-stu-id="d6163-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="d6163-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6163-116">-DefaultProfile</span></span>
<span data-ttu-id="d6163-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d6163-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6163-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d6163-118">-Name</span></span>
<span data-ttu-id="d6163-119">Especifica o nome da configuração IP que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="d6163-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="d6163-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6163-120">CommonParameters</span></span>
<span data-ttu-id="d6163-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6163-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6163-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6163-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6163-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6163-123">INPUTS</span></span>

### <span data-ttu-id="d6163-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6163-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6163-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d6163-125">OUTPUTS</span></span>

### <span data-ttu-id="d6163-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6163-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d6163-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="d6163-127">NOTES</span></span>

## <span data-ttu-id="d6163-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6163-128">RELATED LINKS</span></span>

[<span data-ttu-id="d6163-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6163-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d6163-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6163-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d6163-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6163-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d6163-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6163-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


