---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 1c6a5ffee2f4a8b358f483fee2904fe1a7a970da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426881"
---
# <span data-ttu-id="7c33a-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7c33a-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7c33a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c33a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c33a-103">Modifica uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c33a-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c33a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c33a-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c33a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c33a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c33a-106">O cmdlet **set-AzureRmApplicationGatewayFrontendPort** modifica uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c33a-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="7c33a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c33a-107">EXAMPLES</span></span>

### <span data-ttu-id="7c33a-108">Exemplo 1: definir uma porta de front-end do Application Gateway para o 80</span><span class="sxs-lookup"><span data-stu-id="7c33a-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="7c33a-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7c33a-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="7c33a-110">O segundo comando modifica o gateway em $AppGw para usar a porta 80 para a porta de front-end chamada FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="7c33a-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="7c33a-111">OS</span><span class="sxs-lookup"><span data-stu-id="7c33a-111">PARAMETERS</span></span>

### <span data-ttu-id="7c33a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c33a-112">-ApplicationGateway</span></span>
<span data-ttu-id="7c33a-113">Especifica o objeto do gateway do aplicativo com o qual esse cmdlet associa a porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="7c33a-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="7c33a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c33a-114">-Name</span></span>
<span data-ttu-id="7c33a-115">Especifica o nome da porta de front-end a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="7c33a-115">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="7c33a-116">-Porta</span><span class="sxs-lookup"><span data-stu-id="7c33a-116">-Port</span></span>
<span data-ttu-id="7c33a-117">Especifica o número da porta a ser usada para a porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="7c33a-117">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="7c33a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c33a-118">-DefaultProfile</span></span>
<span data-ttu-id="7c33a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c33a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c33a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c33a-120">CommonParameters</span></span>
<span data-ttu-id="7c33a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c33a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c33a-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c33a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c33a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c33a-123">INPUTS</span></span>

### <span data-ttu-id="7c33a-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c33a-124">PSApplicationGateway</span></span>
<span data-ttu-id="7c33a-125">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7c33a-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7c33a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c33a-126">OUTPUTS</span></span>

### <span data-ttu-id="7c33a-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c33a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7c33a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c33a-128">NOTES</span></span>

## <span data-ttu-id="7c33a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c33a-129">RELATED LINKS</span></span>

[<span data-ttu-id="7c33a-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7c33a-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7c33a-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7c33a-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7c33a-132">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7c33a-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7c33a-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7c33a-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)