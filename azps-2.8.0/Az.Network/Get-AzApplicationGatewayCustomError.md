---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: fbf10b3cfc323a25a7d7a63dc047a4b24141c5d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772062"
---
# <span data-ttu-id="9bf9f-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9bf9f-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9bf9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bf9f-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf9f-103">Obtém erro (s) personalizado (s) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9bf9f-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="9bf9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bf9f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf9f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bf9f-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf9f-106">O cmdlet **Get-AzApplicationGatewayCustomError** Obtém erro (s) personalizado (s) de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9bf9f-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="9bf9f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bf9f-107">EXAMPLES</span></span>

### <span data-ttu-id="9bf9f-108">Exemplo 1: Obtém um erro personalizado em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9bf9f-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="9bf9f-109">Esse comando obtém e retorna o erro personalizado do código de status http 502 da $appgw do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9bf9f-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="9bf9f-110">Exemplo 2: Obtém a lista de todos os erros personalizados em um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="9bf9f-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="9bf9f-111">Esse comando obtém e retorna a lista de todos os erros personalizados do gateway do aplicativo $appgw.</span><span class="sxs-lookup"><span data-stu-id="9bf9f-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="9bf9f-112">OS</span><span class="sxs-lookup"><span data-stu-id="9bf9f-112">PARAMETERS</span></span>

### <span data-ttu-id="9bf9f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bf9f-113">-ApplicationGateway</span></span>
<span data-ttu-id="9bf9f-114">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9bf9f-114">The Application Gateway</span></span>

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

### <span data-ttu-id="9bf9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf9f-115">-DefaultProfile</span></span>
<span data-ttu-id="9bf9f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf9f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf9f-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9bf9f-117">-StatusCode</span></span>
<span data-ttu-id="9bf9f-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="9bf9f-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9bf9f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf9f-119">CommonParameters</span></span>
<span data-ttu-id="9bf9f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf9f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf9f-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf9f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf9f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bf9f-122">INPUTS</span></span>

### <span data-ttu-id="9bf9f-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bf9f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9bf9f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bf9f-124">OUTPUTS</span></span>

### <span data-ttu-id="9bf9f-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9bf9f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9bf9f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bf9f-126">NOTES</span></span>

## <span data-ttu-id="9bf9f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bf9f-127">RELATED LINKS</span></span>

[<span data-ttu-id="9bf9f-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9bf9f-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9bf9f-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9bf9f-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9bf9f-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9bf9f-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="9bf9f-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9bf9f-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
