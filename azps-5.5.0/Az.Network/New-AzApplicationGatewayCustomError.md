---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117426"
---
# <span data-ttu-id="7352c-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7352c-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7352c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7352c-102">SYNOPSIS</span></span>
<span data-ttu-id="7352c-103">Cria um erro personalizado com código de status http e url de página de erro personalizada</span><span class="sxs-lookup"><span data-stu-id="7352c-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="7352c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7352c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7352c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7352c-105">DESCRIPTION</span></span>
<span data-ttu-id="7352c-106">O cmdlet **New-AzApplicationGatewayCustomError** cria um erro personalizado.</span><span class="sxs-lookup"><span data-stu-id="7352c-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="7352c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7352c-107">EXAMPLES</span></span>

### <span data-ttu-id="7352c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7352c-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="7352c-109">Esse comando cria o erro personalizado do código de status http 403.</span><span class="sxs-lookup"><span data-stu-id="7352c-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="7352c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7352c-110">PARAMETERS</span></span>

### <span data-ttu-id="7352c-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="7352c-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="7352c-112">URL da página de erro do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7352c-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7352c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7352c-113">-DefaultProfile</span></span>
<span data-ttu-id="7352c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7352c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7352c-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7352c-115">-StatusCode</span></span>
<span data-ttu-id="7352c-116">Código de status do erro do cliente do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7352c-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7352c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7352c-117">CommonParameters</span></span>
<span data-ttu-id="7352c-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7352c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7352c-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7352c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7352c-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="7352c-120">INPUTS</span></span>

### <span data-ttu-id="7352c-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7352c-121">None</span></span>

## <span data-ttu-id="7352c-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="7352c-122">OUTPUTS</span></span>

### <span data-ttu-id="7352c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7352c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7352c-124">Notas</span><span class="sxs-lookup"><span data-stu-id="7352c-124">NOTES</span></span>

## <span data-ttu-id="7352c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7352c-125">RELATED LINKS</span></span>

[<span data-ttu-id="7352c-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7352c-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7352c-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7352c-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7352c-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7352c-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7352c-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7352c-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
