---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 79b61f5d96307afea47851b210fc1a1ee97acf61
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786089"
---
# <span data-ttu-id="c7201-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7201-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c7201-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7201-102">SYNOPSIS</span></span>
<span data-ttu-id="c7201-103">Obtém a escuta HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7201-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7201-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7201-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7201-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7201-105">DESCRIPTION</span></span>
<span data-ttu-id="c7201-106">O cmdlet **Get-AzureRmApplicationGatewayHttpListener** Obtém a escuta http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7201-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="c7201-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7201-107">EXAMPLES</span></span>

### <span data-ttu-id="c7201-108">Exemplo 1: obter um ouvinte HTTP específico</span><span class="sxs-lookup"><span data-stu-id="c7201-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="c7201-109">Esse comando obtém um ouvinte HTTP chamado Listener01.</span><span class="sxs-lookup"><span data-stu-id="c7201-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="c7201-110">Exemplo 2: obter uma lista de ouvintes HTTP</span><span class="sxs-lookup"><span data-stu-id="c7201-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="c7201-111">Esse comando obtém uma lista de ouvintes HTTP.</span><span class="sxs-lookup"><span data-stu-id="c7201-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="c7201-112">OS</span><span class="sxs-lookup"><span data-stu-id="c7201-112">PARAMETERS</span></span>

### <span data-ttu-id="c7201-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7201-113">-ApplicationGateway</span></span>
<span data-ttu-id="c7201-114">Especifica o objeto do gateway do aplicativo que contém o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="c7201-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="c7201-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7201-115">-DefaultProfile</span></span>
<span data-ttu-id="c7201-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7201-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7201-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7201-117">-Name</span></span>
<span data-ttu-id="c7201-118">Especifica o nome do ouvinte HTTP que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c7201-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="c7201-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7201-119">CommonParameters</span></span>
<span data-ttu-id="c7201-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7201-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7201-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7201-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7201-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7201-122">INPUTS</span></span>

### <span data-ttu-id="c7201-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c7201-123">System.String</span></span>

## <span data-ttu-id="c7201-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7201-124">OUTPUTS</span></span>

### <span data-ttu-id="c7201-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7201-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c7201-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7201-126">NOTES</span></span>

## <span data-ttu-id="c7201-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7201-127">RELATED LINKS</span></span>

[<span data-ttu-id="c7201-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7201-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7201-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7201-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7201-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7201-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7201-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7201-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


