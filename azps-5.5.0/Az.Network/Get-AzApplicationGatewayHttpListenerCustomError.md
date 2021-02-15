---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112911"
---
# <span data-ttu-id="7c92d-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7c92d-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="7c92d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c92d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c92d-103">Obtém erros personalizados de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c92d-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7c92d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c92d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c92d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c92d-105">DESCRIPTION</span></span>
<span data-ttu-id="7c92d-106">O cmdlet **Get-AzApplicationGatewayCustomError** obtém erros personalizados de um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c92d-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7c92d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c92d-107">EXAMPLES</span></span>

### <span data-ttu-id="7c92d-108">Exemplo 1: recebe um erro personalizado em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="7c92d-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="7c92d-109">Esse comando obtém e retorna o erro personalizado do código de status http 502 do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="7c92d-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="7c92d-110">Exemplo 2: Obtém a lista de todos os erros personalizados em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="7c92d-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="7c92d-111">Esse comando obtém e retorna a lista de todos os erros personalizados do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="7c92d-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="7c92d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c92d-112">PARAMETERS</span></span>

### <span data-ttu-id="7c92d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c92d-113">-DefaultProfile</span></span>
<span data-ttu-id="7c92d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c92d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c92d-115">-httpListener</span><span class="sxs-lookup"><span data-stu-id="7c92d-115">-HttpListener</span></span>
<span data-ttu-id="7c92d-116">O gateway de aplicativo http ouvinte</span><span class="sxs-lookup"><span data-stu-id="7c92d-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="7c92d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7c92d-117">-StatusCode</span></span>
<span data-ttu-id="7c92d-118">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c92d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7c92d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c92d-119">CommonParameters</span></span>
<span data-ttu-id="7c92d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c92d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c92d-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c92d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c92d-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="7c92d-122">INPUTS</span></span>

### <span data-ttu-id="7c92d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7c92d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7c92d-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="7c92d-124">OUTPUTS</span></span>

### <span data-ttu-id="7c92d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7c92d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7c92d-126">Notas</span><span class="sxs-lookup"><span data-stu-id="7c92d-126">NOTES</span></span>

## <span data-ttu-id="7c92d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c92d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7c92d-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7c92d-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7c92d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7c92d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7c92d-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7c92d-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
