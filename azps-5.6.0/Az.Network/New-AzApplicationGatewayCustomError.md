---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 377145933832c587691ed30db08754ef1e6f1f64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887876"
---
# <span data-ttu-id="f88e8-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f88e8-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f88e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f88e8-102">SYNOPSIS</span></span>
<span data-ttu-id="f88e8-103">Cria um erro personalizado com código de status http e url de página de erro personalizada</span><span class="sxs-lookup"><span data-stu-id="f88e8-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="f88e8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f88e8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f88e8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f88e8-105">DESCRIPTION</span></span>
<span data-ttu-id="f88e8-106">O cmdlet **New-AzApplicationGatewayCustomError** cria um erro personalizado.</span><span class="sxs-lookup"><span data-stu-id="f88e8-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="f88e8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f88e8-107">EXAMPLES</span></span>

### <span data-ttu-id="f88e8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f88e8-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="f88e8-109">Este comando cria o erro personalizado do código de status http 403.</span><span class="sxs-lookup"><span data-stu-id="f88e8-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="f88e8-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f88e8-110">PARAMETERS</span></span>

### <span data-ttu-id="f88e8-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f88e8-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f88e8-112">URL da página de erro do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f88e8-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f88e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88e8-113">-DefaultProfile</span></span>
<span data-ttu-id="f88e8-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f88e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f88e8-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f88e8-115">-StatusCode</span></span>
<span data-ttu-id="f88e8-116">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f88e8-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f88e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88e8-117">CommonParameters</span></span>
<span data-ttu-id="f88e8-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88e8-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f88e8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88e8-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f88e8-120">INPUTS</span></span>

### <span data-ttu-id="f88e8-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f88e8-121">None</span></span>

## <span data-ttu-id="f88e8-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f88e8-122">OUTPUTS</span></span>

### <span data-ttu-id="f88e8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f88e8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f88e8-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="f88e8-124">NOTES</span></span>

## <span data-ttu-id="f88e8-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f88e8-125">RELATED LINKS</span></span>

[<span data-ttu-id="f88e8-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f88e8-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f88e8-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f88e8-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f88e8-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f88e8-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f88e8-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f88e8-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
