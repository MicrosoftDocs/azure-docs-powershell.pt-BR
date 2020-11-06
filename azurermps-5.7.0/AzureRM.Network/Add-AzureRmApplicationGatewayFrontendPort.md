---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: c9be5f69fc210f68ceb90cfe2e21f5afab164b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432468"
---
# <span data-ttu-id="141d1-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="141d1-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="141d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="141d1-102">SYNOPSIS</span></span>
<span data-ttu-id="141d1-103">Adiciona uma porta de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="141d1-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="141d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="141d1-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="141d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="141d1-105">DESCRIPTION</span></span>
<span data-ttu-id="141d1-106">O cmdlet **Add-AzureRmApplicationGatewayFrontendPort** adiciona uma porta de front-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="141d1-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="141d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="141d1-107">EXAMPLES</span></span>

### <span data-ttu-id="141d1-108">Exemplo 1: adicionar uma porta de front-end a um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="141d1-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="141d1-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="141d1-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="141d1-110">O segundo comando adiciona a porta 80 como uma porta de front-end do gateway do aplicativo armazenado no $AppGw e nomeia a porta FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="141d1-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="141d1-111">OS</span><span class="sxs-lookup"><span data-stu-id="141d1-111">PARAMETERS</span></span>

### <span data-ttu-id="141d1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="141d1-112">-ApplicationGateway</span></span>
<span data-ttu-id="141d1-113">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona uma porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="141d1-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="141d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141d1-114">-DefaultProfile</span></span>
<span data-ttu-id="141d1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="141d1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="141d1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="141d1-116">-Name</span></span>
<span data-ttu-id="141d1-117">Especifica o nome da porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="141d1-117">Specifies the name of the front-end port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141d1-118">-Porta</span><span class="sxs-lookup"><span data-stu-id="141d1-118">-Port</span></span>
<span data-ttu-id="141d1-119">Especifica o número da porta.</span><span class="sxs-lookup"><span data-stu-id="141d1-119">Specifies the port number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141d1-120">CommonParameters</span></span>
<span data-ttu-id="141d1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141d1-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="141d1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141d1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="141d1-123">INPUTS</span></span>

### <span data-ttu-id="141d1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="141d1-124">System.String</span></span>

## <span data-ttu-id="141d1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="141d1-125">OUTPUTS</span></span>

### <span data-ttu-id="141d1-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="141d1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="141d1-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="141d1-127">NOTES</span></span>

## <span data-ttu-id="141d1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="141d1-128">RELATED LINKS</span></span>

[<span data-ttu-id="141d1-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="141d1-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="141d1-130">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="141d1-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="141d1-131">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="141d1-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="141d1-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="141d1-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


