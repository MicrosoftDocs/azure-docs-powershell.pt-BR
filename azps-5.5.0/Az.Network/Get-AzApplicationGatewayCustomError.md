---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114177"
---
# <span data-ttu-id="f9ea6-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f9ea6-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f9ea6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ea6-103">Obtém erros personalizados de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="f9ea6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9ea6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9ea6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9ea6-105">DESCRIPTION</span></span>
<span data-ttu-id="f9ea6-106">O cmdlet **Get-AzApplicationGatewayCustomError** obtém erros personalizados de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="f9ea6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9ea6-107">EXAMPLES</span></span>

### <span data-ttu-id="f9ea6-108">Exemplo 1: recebe um erro personalizado em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f9ea6-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="f9ea6-109">Esse comando obtém e retorna o erro personalizado do código de status http 502 do gateway de aplicativo $appgw.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="f9ea6-110">Exemplo 2: Obtém a lista de todos os erros personalizados em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f9ea6-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="f9ea6-111">Esse comando obtém e retorna a lista de todos os erros personalizados do gateway de aplicativos $appgw.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="f9ea6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9ea6-112">PARAMETERS</span></span>

### <span data-ttu-id="f9ea6-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9ea6-113">-ApplicationGateway</span></span>
<span data-ttu-id="f9ea6-114">O Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f9ea6-114">The Application Gateway</span></span>

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

### <span data-ttu-id="f9ea6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ea6-115">-DefaultProfile</span></span>
<span data-ttu-id="f9ea6-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9ea6-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f9ea6-117">-StatusCode</span></span>
<span data-ttu-id="f9ea6-118">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f9ea6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ea6-119">CommonParameters</span></span>
<span data-ttu-id="f9ea6-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9ea6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ea6-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9ea6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ea6-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9ea6-122">INPUTS</span></span>

### <span data-ttu-id="f9ea6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9ea6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f9ea6-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9ea6-124">OUTPUTS</span></span>

### <span data-ttu-id="f9ea6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f9ea6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f9ea6-126">Notas</span><span class="sxs-lookup"><span data-stu-id="f9ea6-126">NOTES</span></span>

## <span data-ttu-id="f9ea6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9ea6-127">RELATED LINKS</span></span>

[<span data-ttu-id="f9ea6-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f9ea6-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f9ea6-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f9ea6-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f9ea6-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f9ea6-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f9ea6-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f9ea6-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
