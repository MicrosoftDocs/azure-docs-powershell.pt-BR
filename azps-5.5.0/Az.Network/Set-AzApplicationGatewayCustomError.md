---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115068"
---
# <span data-ttu-id="baaaf-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="baaaf-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="baaaf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="baaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="baaaf-103">Atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="baaaf-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="baaaf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baaaf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baaaf-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="baaaf-105">DESCRIPTION</span></span>
<span data-ttu-id="baaaf-106">O cmdlet **Set-AzApplicationGatewayCustomError** atualiza um erro personalizado em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="baaaf-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="baaaf-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="baaaf-107">EXAMPLES</span></span>

### <span data-ttu-id="baaaf-108">Exemplo 1: atualiza o erro personalizado em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="baaaf-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="baaaf-109">Esse comando atualiza o erro personalizado do código de status http 502 no gateway de aplicativos $appgw e retorna o gateway atualizado.</span><span class="sxs-lookup"><span data-stu-id="baaaf-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="baaaf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baaaf-110">PARAMETERS</span></span>

### <span data-ttu-id="baaaf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="baaaf-111">-ApplicationGateway</span></span>
<span data-ttu-id="baaaf-112">O Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="baaaf-112">The Application Gateway</span></span>

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

### <span data-ttu-id="baaaf-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="baaaf-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="baaaf-114">URL da página de erro do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="baaaf-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="baaaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baaaf-115">-DefaultProfile</span></span>
<span data-ttu-id="baaaf-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baaaf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baaaf-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="baaaf-117">-StatusCode</span></span>
<span data-ttu-id="baaaf-118">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="baaaf-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="baaaf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaaf-119">CommonParameters</span></span>
<span data-ttu-id="baaaf-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baaaf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaaf-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baaaf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaaf-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="baaaf-122">INPUTS</span></span>

### <span data-ttu-id="baaaf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="baaaf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="baaaf-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="baaaf-124">OUTPUTS</span></span>

### <span data-ttu-id="baaaf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="baaaf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="baaaf-126">Notas</span><span class="sxs-lookup"><span data-stu-id="baaaf-126">NOTES</span></span>

## <span data-ttu-id="baaaf-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baaaf-127">RELATED LINKS</span></span>

[<span data-ttu-id="baaaf-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="baaaf-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="baaaf-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="baaaf-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="baaaf-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="baaaf-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="baaaf-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="baaaf-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
