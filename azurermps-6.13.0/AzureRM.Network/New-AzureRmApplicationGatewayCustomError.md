---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433205"
---
# <span data-ttu-id="90789-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="90789-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="90789-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90789-102">SYNOPSIS</span></span>
<span data-ttu-id="90789-103">Cria um erro personalizado com código de status HTTP e URL da página de erro personalizada</span><span class="sxs-lookup"><span data-stu-id="90789-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90789-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90789-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90789-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90789-105">DESCRIPTION</span></span>
<span data-ttu-id="90789-106">O cmdlet **New-AzureRmApplicationGatewayCustomError** cria um erro personalizado.</span><span class="sxs-lookup"><span data-stu-id="90789-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="90789-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90789-107">EXAMPLES</span></span>

### <span data-ttu-id="90789-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90789-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="90789-109">Esse comando cria o erro personalizado de código de status HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="90789-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="90789-110">OS</span><span class="sxs-lookup"><span data-stu-id="90789-110">PARAMETERS</span></span>

### <span data-ttu-id="90789-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="90789-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="90789-112">URL da página de erro do erro do cliente do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="90789-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90789-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90789-113">-DefaultProfile</span></span>
<span data-ttu-id="90789-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90789-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90789-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="90789-115">-StatusCode</span></span>
<span data-ttu-id="90789-116">Código do status do erro do cliente do aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="90789-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90789-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90789-117">CommonParameters</span></span>
<span data-ttu-id="90789-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90789-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="90789-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90789-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90789-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90789-120">INPUTS</span></span>

### <span data-ttu-id="90789-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="90789-121">None</span></span>

## <span data-ttu-id="90789-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90789-122">OUTPUTS</span></span>

### <span data-ttu-id="90789-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="90789-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="90789-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90789-124">NOTES</span></span>

## <span data-ttu-id="90789-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90789-125">RELATED LINKS</span></span>
