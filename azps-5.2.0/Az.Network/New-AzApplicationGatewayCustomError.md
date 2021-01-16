---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259433"
---
# <span data-ttu-id="59622-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="59622-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="59622-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59622-102">SYNOPSIS</span></span>
<span data-ttu-id="59622-103">Cria um erro personalizado com código de status HTTP e URL da página de erro personalizada</span><span class="sxs-lookup"><span data-stu-id="59622-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="59622-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59622-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59622-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59622-105">DESCRIPTION</span></span>
<span data-ttu-id="59622-106">O cmdlet **New-AzApplicationGatewayCustomError** cria um erro personalizado.</span><span class="sxs-lookup"><span data-stu-id="59622-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="59622-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59622-107">EXAMPLES</span></span>

### <span data-ttu-id="59622-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59622-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="59622-109">Esse comando cria o erro personalizado de código de status HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="59622-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="59622-110">OS</span><span class="sxs-lookup"><span data-stu-id="59622-110">PARAMETERS</span></span>

### <span data-ttu-id="59622-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="59622-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="59622-112">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59622-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="59622-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59622-113">-DefaultProfile</span></span>
<span data-ttu-id="59622-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59622-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59622-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="59622-115">-StatusCode</span></span>
<span data-ttu-id="59622-116">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="59622-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="59622-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59622-117">CommonParameters</span></span>
<span data-ttu-id="59622-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59622-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59622-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59622-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59622-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59622-120">INPUTS</span></span>

### <span data-ttu-id="59622-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="59622-121">None</span></span>

## <span data-ttu-id="59622-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59622-122">OUTPUTS</span></span>

### <span data-ttu-id="59622-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="59622-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="59622-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59622-124">NOTES</span></span>

## <span data-ttu-id="59622-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59622-125">RELATED LINKS</span></span>

[<span data-ttu-id="59622-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="59622-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="59622-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="59622-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="59622-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="59622-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="59622-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="59622-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
