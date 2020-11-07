---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: c138ced515932d158bb2a4a067ed405d8084db4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785718"
---
# <span data-ttu-id="8b471-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8b471-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="8b471-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b471-102">SYNOPSIS</span></span>
<span data-ttu-id="8b471-103">Obtém a configuração de IP de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b471-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b471-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b471-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b471-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b471-105">DESCRIPTION</span></span>
<span data-ttu-id="8b471-106">O cmdlet **Get-AzureRmApplicationGatewayFrontendIPConfig** Obtém a configuração de IP de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b471-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="8b471-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b471-107">EXAMPLES</span></span>

### <span data-ttu-id="8b471-108">Exemplo 1: obter uma configuração de IP front-end especificada</span><span class="sxs-lookup"><span data-stu-id="8b471-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="8b471-109">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém a configuração de IP de front-end chamada FrontEndIP01 da $AppGw e a armazena na variável $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="8b471-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="8b471-110">Exemplo 2: obter uma lista de configurações de IP front-end</span><span class="sxs-lookup"><span data-stu-id="8b471-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="8b471-111">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém uma lista das configurações de IP de front-end da $AppGw e a armazena na variável $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="8b471-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="8b471-112">OS</span><span class="sxs-lookup"><span data-stu-id="8b471-112">PARAMETERS</span></span>

### <span data-ttu-id="8b471-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b471-113">-ApplicationGateway</span></span>
<span data-ttu-id="8b471-114">Especifica o objeto do gateway do aplicativo que contém a configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="8b471-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b471-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b471-115">-DefaultProfile</span></span>
<span data-ttu-id="8b471-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b471-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b471-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b471-117">-Name</span></span>
<span data-ttu-id="8b471-118">Especifica o nome da configuração de IP de front-end que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8b471-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b471-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b471-119">CommonParameters</span></span>
<span data-ttu-id="8b471-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b471-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b471-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b471-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b471-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b471-122">INPUTS</span></span>

### <span data-ttu-id="8b471-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8b471-123">System.String</span></span>

## <span data-ttu-id="8b471-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b471-124">OUTPUTS</span></span>

### <span data-ttu-id="8b471-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b471-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="8b471-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b471-126">NOTES</span></span>

## <span data-ttu-id="8b471-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b471-127">RELATED LINKS</span></span>

[<span data-ttu-id="8b471-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8b471-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8b471-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8b471-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8b471-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8b471-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8b471-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8b471-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


