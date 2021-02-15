---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111563"
---
# <span data-ttu-id="c52ec-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c52ec-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="c52ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c52ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c52ec-103">Atualiza um erro personalizado em um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c52ec-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="c52ec-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c52ec-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c52ec-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c52ec-105">DESCRIPTION</span></span>
<span data-ttu-id="c52ec-106">O cmdlet **Set-AzApplicationGatewayCustomError** atualiza um erro personalizado em um ouvinte http de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c52ec-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="c52ec-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c52ec-107">EXAMPLES</span></span>

### <span data-ttu-id="c52ec-108">Exemplo 1: atualiza um erro personalizado de um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="c52ec-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="c52ec-109">Este comando atualiza o erro personalizado do código de status http 502 no ouvinte http $listener 01 e retorna o ouvinte atualizado.</span><span class="sxs-lookup"><span data-stu-id="c52ec-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="c52ec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c52ec-110">PARAMETERS</span></span>

### <span data-ttu-id="c52ec-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c52ec-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c52ec-112">URL da página de erro do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c52ec-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c52ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52ec-113">-DefaultProfile</span></span>
<span data-ttu-id="c52ec-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c52ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c52ec-115">-httpListener</span><span class="sxs-lookup"><span data-stu-id="c52ec-115">-HttpListener</span></span>
<span data-ttu-id="c52ec-116">O gateway de aplicativo http ouvinte</span><span class="sxs-lookup"><span data-stu-id="c52ec-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="c52ec-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c52ec-117">-StatusCode</span></span>
<span data-ttu-id="c52ec-118">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c52ec-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c52ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52ec-119">CommonParameters</span></span>
<span data-ttu-id="c52ec-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c52ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52ec-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c52ec-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52ec-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="c52ec-122">INPUTS</span></span>

### <span data-ttu-id="c52ec-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c52ec-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c52ec-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="c52ec-124">OUTPUTS</span></span>

### <span data-ttu-id="c52ec-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c52ec-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c52ec-126">Notas</span><span class="sxs-lookup"><span data-stu-id="c52ec-126">NOTES</span></span>

## <span data-ttu-id="c52ec-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c52ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="c52ec-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c52ec-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="c52ec-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c52ec-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="c52ec-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c52ec-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
