---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: a59646c6214b3c4372eef9def61f67fe4a5bd912
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600062"
---
# <span data-ttu-id="e6f52-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e6f52-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e6f52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6f52-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f52-103">Atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6f52-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="e6f52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6f52-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6f52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6f52-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f52-106">O cmdlet **set-AzApplicationGatewayCustomError** atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6f52-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="e6f52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6f52-107">EXAMPLES</span></span>

### <span data-ttu-id="e6f52-108">Exemplo 1: atualiza o erro personalizado em um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="e6f52-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="e6f52-109">Esse comando atualiza o erro personalizado do código de status http 502 na $appgw do gateway do aplicativo e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="e6f52-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="e6f52-110">OS</span><span class="sxs-lookup"><span data-stu-id="e6f52-110">PARAMETERS</span></span>

### <span data-ttu-id="e6f52-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6f52-111">-ApplicationGateway</span></span>
<span data-ttu-id="e6f52-112">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e6f52-112">The Application Gateway</span></span>

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

### <span data-ttu-id="e6f52-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e6f52-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e6f52-114">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6f52-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e6f52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f52-115">-DefaultProfile</span></span>
<span data-ttu-id="e6f52-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f52-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e6f52-117">-StatusCode</span></span>
<span data-ttu-id="e6f52-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="e6f52-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e6f52-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f52-119">CommonParameters</span></span>
<span data-ttu-id="e6f52-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f52-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f52-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f52-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f52-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6f52-122">INPUTS</span></span>

### <span data-ttu-id="e6f52-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6f52-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6f52-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6f52-124">OUTPUTS</span></span>

### <span data-ttu-id="e6f52-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e6f52-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e6f52-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6f52-126">NOTES</span></span>

## <span data-ttu-id="e6f52-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6f52-127">RELATED LINKS</span></span>

[<span data-ttu-id="e6f52-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e6f52-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e6f52-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e6f52-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e6f52-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e6f52-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e6f52-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e6f52-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
