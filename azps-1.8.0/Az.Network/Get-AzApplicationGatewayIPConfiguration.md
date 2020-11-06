---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 16df8726fc0018bbc89dfbee025223b9e35792c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600644"
---
# <span data-ttu-id="e5969-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5969-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e5969-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5969-102">SYNOPSIS</span></span>
<span data-ttu-id="e5969-103">Obtém a configuração de IP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5969-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="e5969-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5969-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5969-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5969-105">DESCRIPTION</span></span>
<span data-ttu-id="e5969-106">O cmdlet **Get-AzApplicationGatewayIPConfiguration** Obtém a configuração de IP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5969-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="e5969-107">A configuração de IP contém a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="e5969-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="e5969-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5969-108">EXAMPLES</span></span>

### <span data-ttu-id="e5969-109">Exemplo 1: obter uma configuração de IP específica</span><span class="sxs-lookup"><span data-stu-id="e5969-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e5969-110">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw. O segundo comando obtém uma configuração de IP chamada GateSubnet01 do gateway armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e5969-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="e5969-111">Exemplo 2: obter uma lista de configurações de IP</span><span class="sxs-lookup"><span data-stu-id="e5969-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="e5969-112">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw. O segundo comando obtém uma lista de todas as configurações de IP.</span><span class="sxs-lookup"><span data-stu-id="e5969-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="e5969-113">OS</span><span class="sxs-lookup"><span data-stu-id="e5969-113">PARAMETERS</span></span>

### <span data-ttu-id="e5969-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5969-114">-ApplicationGateway</span></span>
<span data-ttu-id="e5969-115">Especifica o objeto do gateway do aplicativo que contém a configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="e5969-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="e5969-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5969-116">-DefaultProfile</span></span>
<span data-ttu-id="e5969-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5969-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5969-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5969-118">-Name</span></span>
<span data-ttu-id="e5969-119">Especifica o nome da configuração de IP que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e5969-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="e5969-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5969-120">CommonParameters</span></span>
<span data-ttu-id="e5969-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5969-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5969-122">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5969-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5969-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5969-123">INPUTS</span></span>

### <span data-ttu-id="e5969-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5969-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5969-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5969-125">OUTPUTS</span></span>

### <span data-ttu-id="e5969-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5969-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e5969-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5969-127">NOTES</span></span>

## <span data-ttu-id="e5969-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5969-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5969-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5969-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e5969-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5969-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e5969-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5969-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e5969-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5969-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


