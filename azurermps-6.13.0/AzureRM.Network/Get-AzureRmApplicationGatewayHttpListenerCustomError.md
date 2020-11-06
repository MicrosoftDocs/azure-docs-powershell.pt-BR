---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 89e323bd8e8dedbaa3c7716a6c10119a6fb69365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430178"
---
# <span data-ttu-id="ede10-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ede10-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="ede10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ede10-102">SYNOPSIS</span></span>
<span data-ttu-id="ede10-103">Obtém erro (s) personalizado (s) de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ede10-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ede10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ede10-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ede10-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ede10-105">DESCRIPTION</span></span>
<span data-ttu-id="ede10-106">O cmdlet **Get-AzureRmApplicationGatewayCustomError** Obtém erro (s) personalizado (s) de um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ede10-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="ede10-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ede10-107">EXAMPLES</span></span>

### <span data-ttu-id="ede10-108">Exemplo 1: Obtém um erro personalizado em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="ede10-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="ede10-109">Esse comando obtém e retorna o erro personalizado do código de status http 502 do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="ede10-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="ede10-110">Exemplo 2: Obtém a lista de todos os erros personalizados em um ouvinte http</span><span class="sxs-lookup"><span data-stu-id="ede10-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="ede10-111">Esse comando obtém e retorna a lista de todos os erros personalizados do ouvinte http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="ede10-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="ede10-112">OS</span><span class="sxs-lookup"><span data-stu-id="ede10-112">PARAMETERS</span></span>

### <span data-ttu-id="ede10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede10-113">-DefaultProfile</span></span>
<span data-ttu-id="ede10-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ede10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ede10-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="ede10-115">-HttpListener</span></span>
<span data-ttu-id="ede10-116">Ouvinte http do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ede10-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ede10-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ede10-117">-StatusCode</span></span>
<span data-ttu-id="ede10-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="ede10-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ede10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede10-119">CommonParameters</span></span>
<span data-ttu-id="ede10-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ede10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ede10-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ede10-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede10-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ede10-122">INPUTS</span></span>

### <span data-ttu-id="ede10-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ede10-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ede10-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ede10-124">OUTPUTS</span></span>

### <span data-ttu-id="ede10-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ede10-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ede10-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ede10-126">NOTES</span></span>

## <span data-ttu-id="ede10-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ede10-127">RELATED LINKS</span></span>
