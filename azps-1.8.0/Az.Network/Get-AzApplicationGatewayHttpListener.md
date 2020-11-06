---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91b2791b7f61c7586c1fbd4bca954e374ccbb43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600648"
---
# <span data-ttu-id="d5a1c-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d5a1c-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d5a1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a1c-103">Obtém a escuta HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="d5a1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5a1c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a1c-106">O cmdlet **Get-AzApplicationGatewayHttpListener** Obtém a escuta http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="d5a1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a1c-108">Exemplo 1: obter um ouvinte HTTP específico</span><span class="sxs-lookup"><span data-stu-id="d5a1c-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="d5a1c-109">Esse comando obtém um ouvinte HTTP chamado Listener01.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="d5a1c-110">Exemplo 2: obter uma lista de ouvintes HTTP</span><span class="sxs-lookup"><span data-stu-id="d5a1c-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="d5a1c-111">Esse comando obtém uma lista de ouvintes HTTP.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="d5a1c-112">OS</span><span class="sxs-lookup"><span data-stu-id="d5a1c-112">PARAMETERS</span></span>

### <span data-ttu-id="d5a1c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5a1c-113">-ApplicationGateway</span></span>
<span data-ttu-id="d5a1c-114">Especifica o objeto do gateway do aplicativo que contém o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="d5a1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a1c-115">-DefaultProfile</span></span>
<span data-ttu-id="d5a1c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a1c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5a1c-117">-Name</span></span>
<span data-ttu-id="d5a1c-118">Especifica o nome do ouvinte HTTP que o cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5a1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a1c-119">CommonParameters</span></span>
<span data-ttu-id="d5a1c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a1c-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5a1c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a1c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5a1c-122">INPUTS</span></span>

### <span data-ttu-id="d5a1c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5a1c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5a1c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5a1c-124">OUTPUTS</span></span>

### <span data-ttu-id="d5a1c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d5a1c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d5a1c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5a1c-126">NOTES</span></span>

## <span data-ttu-id="d5a1c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5a1c-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5a1c-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d5a1c-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d5a1c-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d5a1c-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d5a1c-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d5a1c-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="d5a1c-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d5a1c-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


