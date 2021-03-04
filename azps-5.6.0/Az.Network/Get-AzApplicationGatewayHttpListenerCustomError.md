---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891804"
---
# <span data-ttu-id="b7212-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b7212-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="b7212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7212-102">SYNOPSIS</span></span>
<span data-ttu-id="b7212-103">Obtém erros personalizados de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7212-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="b7212-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7212-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7212-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7212-105">DESCRIPTION</span></span>
<span data-ttu-id="b7212-106">O cmdlet **Get-AzApplicationGatewayCustomError** obtém erros personalizados de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7212-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="b7212-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7212-107">EXAMPLES</span></span>

### <span data-ttu-id="b7212-108">Exemplo 1: obtém um erro personalizado em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="b7212-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="b7212-109">Este comando obtém e retorna o erro personalizado do código de status http 502 do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="b7212-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="b7212-110">Exemplo 2: Obtém a lista de todos os erros personalizados em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="b7212-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="b7212-111">Este comando obtém e retorna a lista de todos os erros personalizados do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="b7212-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="b7212-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7212-112">PARAMETERS</span></span>

### <span data-ttu-id="b7212-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7212-113">-DefaultProfile</span></span>
<span data-ttu-id="b7212-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7212-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7212-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b7212-115">-HttpListener</span></span>
<span data-ttu-id="b7212-116">O Ouvinte Http do Gateway de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="b7212-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7212-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b7212-117">-StatusCode</span></span>
<span data-ttu-id="b7212-118">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7212-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b7212-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7212-119">CommonParameters</span></span>
<span data-ttu-id="b7212-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7212-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7212-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7212-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7212-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7212-122">INPUTS</span></span>

### <span data-ttu-id="b7212-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b7212-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b7212-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7212-124">OUTPUTS</span></span>

### <span data-ttu-id="b7212-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b7212-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b7212-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7212-126">NOTES</span></span>

## <span data-ttu-id="b7212-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7212-127">RELATED LINKS</span></span>

[<span data-ttu-id="b7212-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b7212-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b7212-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b7212-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b7212-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b7212-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
