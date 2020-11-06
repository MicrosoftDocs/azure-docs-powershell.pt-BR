---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 8995c91484bba1c11944bf9d2a6e3dbc8ff5738d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440767"
---
# <span data-ttu-id="96547-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96547-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="96547-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96547-102">SYNOPSIS</span></span>
<span data-ttu-id="96547-103">Obtém a configuração de IP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96547-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96547-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96547-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96547-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96547-105">DESCRIPTION</span></span>
<span data-ttu-id="96547-106">O cmdlet **Get-AzureRmApplicationGatewayIPConfiguration** Obtém a configuração de IP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96547-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="96547-107">A configuração de IP contém a sub-rede na qual o Application Gateway é implantado.</span><span class="sxs-lookup"><span data-stu-id="96547-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="96547-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96547-108">EXAMPLES</span></span>

### <span data-ttu-id="96547-109">Exemplo 1: obter uma configuração de IP específica</span><span class="sxs-lookup"><span data-stu-id="96547-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="96547-110">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw. O segundo comando obtém uma configuração de IP chamada GateSubnet01 do gateway armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="96547-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="96547-111">Exemplo 2: obter uma lista de configurações de IP</span><span class="sxs-lookup"><span data-stu-id="96547-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="96547-112">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw. O segundo comando obtém uma lista de todas as configurações de IP.</span><span class="sxs-lookup"><span data-stu-id="96547-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="96547-113">OS</span><span class="sxs-lookup"><span data-stu-id="96547-113">PARAMETERS</span></span>

### <span data-ttu-id="96547-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96547-114">-ApplicationGateway</span></span>
<span data-ttu-id="96547-115">Especifica o objeto do gateway do aplicativo que contém a configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="96547-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="96547-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96547-116">-DefaultProfile</span></span>
<span data-ttu-id="96547-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96547-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96547-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="96547-118">-Name</span></span>
<span data-ttu-id="96547-119">Especifica o nome da configuração de IP que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="96547-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="96547-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96547-120">CommonParameters</span></span>
<span data-ttu-id="96547-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96547-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96547-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96547-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96547-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96547-123">INPUTS</span></span>

### <span data-ttu-id="96547-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96547-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="96547-125">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96547-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="96547-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96547-126">OUTPUTS</span></span>

### <span data-ttu-id="96547-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96547-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="96547-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96547-128">NOTES</span></span>

## <span data-ttu-id="96547-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96547-129">RELATED LINKS</span></span>

[<span data-ttu-id="96547-130">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96547-130">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96547-131">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96547-131">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96547-132">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96547-132">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="96547-133">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="96547-133">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


