---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117485"
---
# <span data-ttu-id="ff204-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ff204-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="ff204-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff204-102">SYNOPSIS</span></span>
<span data-ttu-id="ff204-103">Adiciona um erro personalizado a um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ff204-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="ff204-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff204-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff204-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff204-105">DESCRIPTION</span></span>
<span data-ttu-id="ff204-106">O cmdlet **Add-AzApplicationGatewayCustomError** adiciona um erro personalizado a um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ff204-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="ff204-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff204-107">EXAMPLES</span></span>

### <span data-ttu-id="ff204-108">Exemplo 1: adiciona um erro personalizado ao nível do ouvinte http</span><span class="sxs-lookup"><span data-stu-id="ff204-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="ff204-109">Este comando adiciona um erro personalizado do código de status http 502 ao ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="ff204-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="ff204-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff204-110">PARAMETERS</span></span>

### <span data-ttu-id="ff204-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="ff204-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="ff204-112">URL da página de erro do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ff204-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ff204-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff204-113">-DefaultProfile</span></span>
<span data-ttu-id="ff204-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff204-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff204-115">-httpListener</span><span class="sxs-lookup"><span data-stu-id="ff204-115">-HttpListener</span></span>
<span data-ttu-id="ff204-116">O gateway de aplicativo http ouvinte</span><span class="sxs-lookup"><span data-stu-id="ff204-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="ff204-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ff204-117">-StatusCode</span></span>
<span data-ttu-id="ff204-118">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ff204-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ff204-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff204-119">CommonParameters</span></span>
<span data-ttu-id="ff204-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff204-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff204-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff204-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff204-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="ff204-122">INPUTS</span></span>

### <span data-ttu-id="ff204-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ff204-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ff204-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="ff204-124">OUTPUTS</span></span>

### <span data-ttu-id="ff204-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ff204-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ff204-126">Notas</span><span class="sxs-lookup"><span data-stu-id="ff204-126">NOTES</span></span>

## <span data-ttu-id="ff204-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff204-127">RELATED LINKS</span></span>

[<span data-ttu-id="ff204-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ff204-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="ff204-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ff204-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="ff204-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ff204-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
