---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e849d4c7eaf007a6e2fd8d6cbbda1cc49cbf2fb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891170"
---
# <span data-ttu-id="be0c4-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="be0c4-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="be0c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="be0c4-103">Obtém o ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be0c4-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="be0c4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be0c4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be0c4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="be0c4-106">O cmdlet **Get-AzApplicationGatewayHttpListener obtém** o ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be0c4-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="be0c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be0c4-107">EXAMPLES</span></span>

### <span data-ttu-id="be0c4-108">Exemplo 1: Obter um ouvinte HTTP específico</span><span class="sxs-lookup"><span data-stu-id="be0c4-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="be0c4-109">Este comando obtém um ouvinte HTTP chamado Listener01.</span><span class="sxs-lookup"><span data-stu-id="be0c4-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="be0c4-110">Exemplo 2: Obter uma lista de ouvintes HTTP</span><span class="sxs-lookup"><span data-stu-id="be0c4-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="be0c4-111">Este comando obtém uma lista de ouvintes HTTP.</span><span class="sxs-lookup"><span data-stu-id="be0c4-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="be0c4-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be0c4-112">PARAMETERS</span></span>

### <span data-ttu-id="be0c4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be0c4-113">-ApplicationGateway</span></span>
<span data-ttu-id="be0c4-114">Especifica o objeto gateway de aplicativo que contém o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="be0c4-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="be0c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0c4-115">-DefaultProfile</span></span>
<span data-ttu-id="be0c4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="be0c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be0c4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="be0c4-117">-Name</span></span>
<span data-ttu-id="be0c4-118">Especifica o nome do ouvinte HTTP que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="be0c4-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="be0c4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0c4-119">CommonParameters</span></span>
<span data-ttu-id="be0c4-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be0c4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0c4-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be0c4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0c4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be0c4-122">INPUTS</span></span>

### <span data-ttu-id="be0c4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be0c4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="be0c4-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be0c4-124">OUTPUTS</span></span>

### <span data-ttu-id="be0c4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="be0c4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="be0c4-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="be0c4-126">NOTES</span></span>

## <span data-ttu-id="be0c4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be0c4-127">RELATED LINKS</span></span>

[<span data-ttu-id="be0c4-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="be0c4-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="be0c4-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="be0c4-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="be0c4-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="be0c4-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="be0c4-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="be0c4-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


