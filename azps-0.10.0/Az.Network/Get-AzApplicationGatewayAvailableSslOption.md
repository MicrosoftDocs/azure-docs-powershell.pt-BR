---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableSslOption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: e0fa27a99a8a2d00819d558b42218b9405a5f039
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775605"
---
# <span data-ttu-id="af122-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="af122-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="af122-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af122-102">SYNOPSIS</span></span>
<span data-ttu-id="af122-103">Obtém todas as opções de SSL disponíveis para a política SSL do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="af122-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="af122-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af122-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af122-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af122-105">DESCRIPTION</span></span>
<span data-ttu-id="af122-106">O cmdlet **Get-AzApplicationGatewayAvailableSslOption** obtém todas as opções SSL disponíveis para a política SSL</span><span class="sxs-lookup"><span data-stu-id="af122-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="af122-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af122-107">EXAMPLES</span></span>

### <span data-ttu-id="af122-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af122-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="af122-109">Esses comandos retornam todas as opções SSL disponíveis para a política SSL.</span><span class="sxs-lookup"><span data-stu-id="af122-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="af122-110">OS</span><span class="sxs-lookup"><span data-stu-id="af122-110">PARAMETERS</span></span>

### <span data-ttu-id="af122-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af122-111">-DefaultProfile</span></span>
<span data-ttu-id="af122-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af122-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af122-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af122-113">CommonParameters</span></span>
<span data-ttu-id="af122-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af122-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af122-115">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af122-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af122-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af122-116">INPUTS</span></span>

### <span data-ttu-id="af122-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="af122-117">None</span></span>

## <span data-ttu-id="af122-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af122-118">OUTPUTS</span></span>

### <span data-ttu-id="af122-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="af122-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="af122-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af122-120">NOTES</span></span>

## <span data-ttu-id="af122-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af122-121">RELATED LINKS</span></span>

