---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610286"
---
# <span data-ttu-id="7adbd-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7adbd-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7adbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7adbd-102">SYNOPSIS</span></span>
<span data-ttu-id="7adbd-103">Obtém erro (s) personalizado (s) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7adbd-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7adbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7adbd-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7adbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7adbd-105">DESCRIPTION</span></span>
<span data-ttu-id="7adbd-106">O cmdlet **Get-AzureRmApplicationGatewayCustomError** Obtém erro (s) personalizado (s) de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7adbd-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="7adbd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7adbd-107">EXAMPLES</span></span>

### <span data-ttu-id="7adbd-108">Exemplo 1: Obtém um erro personalizado em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7adbd-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="7adbd-109">Esse comando obtém e retorna o erro personalizado do código de status http 502 da $appgw do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7adbd-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="7adbd-110">Exemplo 2: Obtém a lista de todos os erros personalizados em um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7adbd-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="7adbd-111">Esse comando obtém e retorna a lista de todos os erros personalizados do gateway do aplicativo $appgw.</span><span class="sxs-lookup"><span data-stu-id="7adbd-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="7adbd-112">OS</span><span class="sxs-lookup"><span data-stu-id="7adbd-112">PARAMETERS</span></span>

### <span data-ttu-id="7adbd-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7adbd-113">-ApplicationGateway</span></span>
<span data-ttu-id="7adbd-114">O Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7adbd-114">The Application Gateway</span></span>

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

### <span data-ttu-id="7adbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adbd-115">-DefaultProfile</span></span>
<span data-ttu-id="7adbd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7adbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adbd-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7adbd-117">-StatusCode</span></span>
<span data-ttu-id="7adbd-118">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="7adbd-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7adbd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adbd-119">CommonParameters</span></span>
<span data-ttu-id="7adbd-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adbd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adbd-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adbd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adbd-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7adbd-122">INPUTS</span></span>

### <span data-ttu-id="7adbd-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7adbd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7adbd-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7adbd-124">OUTPUTS</span></span>

### <span data-ttu-id="7adbd-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7adbd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7adbd-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7adbd-126">NOTES</span></span>

## <span data-ttu-id="7adbd-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7adbd-127">RELATED LINKS</span></span>
