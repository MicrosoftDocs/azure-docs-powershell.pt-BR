---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c06b78062500ddb5c33353c00814a46e919bd8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889911"
---
# <span data-ttu-id="36a7d-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="36a7d-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="36a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="36a7d-103">Atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36a7d-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="36a7d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="36a7d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36a7d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="36a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="36a7d-106">O cmdlet **Set-AzApplicationGatewayCustomError** atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36a7d-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="36a7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36a7d-107">EXAMPLES</span></span>

### <span data-ttu-id="36a7d-108">Exemplo 1: atualiza o erro personalizado em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="36a7d-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="36a7d-109">Este comando atualiza o erro personalizado do código de status http 502 no gateway de aplicativo $appgw e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="36a7d-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="36a7d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="36a7d-110">PARAMETERS</span></span>

### <span data-ttu-id="36a7d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36a7d-111">-ApplicationGateway</span></span>
<span data-ttu-id="36a7d-112">O Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="36a7d-112">The Application Gateway</span></span>

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

### <span data-ttu-id="36a7d-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="36a7d-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="36a7d-114">URL da página de erro do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36a7d-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="36a7d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a7d-115">-DefaultProfile</span></span>
<span data-ttu-id="36a7d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36a7d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36a7d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="36a7d-117">-StatusCode</span></span>
<span data-ttu-id="36a7d-118">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36a7d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="36a7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a7d-119">CommonParameters</span></span>
<span data-ttu-id="36a7d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a7d-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a7d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a7d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36a7d-122">INPUTS</span></span>

### <span data-ttu-id="36a7d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36a7d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36a7d-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="36a7d-124">OUTPUTS</span></span>

### <span data-ttu-id="36a7d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="36a7d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="36a7d-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="36a7d-126">NOTES</span></span>

## <span data-ttu-id="36a7d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36a7d-127">RELATED LINKS</span></span>

[<span data-ttu-id="36a7d-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="36a7d-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="36a7d-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="36a7d-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="36a7d-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="36a7d-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="36a7d-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="36a7d-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
